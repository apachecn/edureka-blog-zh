# 在在线测验应用程序中实现 JavaScript 倒计时定时器

> 原文：<https://www.edureka.co/blog/creating-an-online-quiz-application-implementing-countdown-timer/>

在这篇文章中，我们将扩展我们的测验应用程序，并在其中添加一个 JavaScript 倒计时功能。这里我们要实现的另一件事是，添加代码以便每个测验可以有不同数量的问题。如果你还没有读过第一部分，我建议你通读一遍。你会更容易关注这篇文章并完全理解它。

你可以在这里阅读第一部分 [使用 JSP Servlet](https://www.edureka.co/blog/creating-an-online-quiz-application-using-jsp-servlet/ "Creating an Online Quiz Application") 创建在线测验应用程序。 您还可以通过参加 ***[Angular 认证培训](https://www.edureka.co/angular-training)*** 来拓展您的 Angular 职业机会。

## JavaScript 倒计时定时器

每个测验的持续时间存储在测验 XML 文件中，我们检索测验的持续时间，并将其作为属性保存在用户会话中。当用户提交一个问题时，我们也使用 JavaScript 的自定义表单提交将时间提交给控制器。因此，当我们显示下一个问题时，我们会显示正确的剩余时间。

[![javascript-countdown-timer-online-quiz-application](img/051f179274b0469b5977f15946bbd599.png "Countdown Timer")](https://www.edureka.co/java-j2ee-soa-training)

当测验的持续时间结束时，将向用户显示一个警告框，提示“时间到了”，将对测验进行评估并显示最终结果。

[![javascript-countdown-timer-online-quiz-application](img/75ccd555354135400e21c11eb4bda93a.png "Online Quiz Timer")](https://www.edureka.co/java-j2ee-soa-training)

让我们看看我们需要什么来实现这一点。

我们在测验 XML 文件中的测验问题之前添加了两行新内容。

```
< quiz>
  < title>Java Quiz (2015/01/18)< /title>
  < totalquizquestions>10< /totalquizquestions>
  < quizduration>2< /quizduration>
    < questions>

      < question>
        < quizquestion>Which is the correct syntax ?< /quizquestion>
        < answer> public class ABC extends QWE extends Student< /answer>
        < answer> int i="A";< /answer>
        < answer>String s="Hello";< /answer>
        < answer> private class ABC< /answer>
        < correct>2< /correct>
      < /question>

      < question>
        < quizquestion> Which of the following a is not a keyword in Java ?< /quizquestion>
        < answer>class< /answer>
        < answer>interface< /answer>
        < answer>extends< /answer>
        < answer>abstraction< /answer>
        < correct>3< /correct>
      < /question>

      < question>
        < quizquestion>What is true about Java ?< /quizquestion>
        < answer>Java is platform specific< /answer>
        < answer>Java does not support multiple inheritance< /answer>
        < answer>Java does not run on Linux and Mac< /answer>
        < answer>Java is not a multi-threaded language < /answer>
        < correct>1< /correct>
      < /question>

      < question>
        < quizquestion>Which of the following is an interface ?< /quizquestion>
        < answer>Thread< /answer>
        < answer>Runnable< /answer>
        < answer>Date< /answer>
        < answer>Calendar< /answer>
        < correct>1< /correct>
      < /question>	

	  < question>
        < quizquestion>Which company released Java Version 8 ?< /quizquestion>
        < answer>Sun< /answer>
        < answer>Oracle< /answer>
        < answer>Adobe< /answer>
        < answer>Google< /answer>
        < correct>1< /correct>
      < /question>

     < question>
        < quizquestion>Java comes under which category of languages ?< /quizquestion>
        < answer>First Generation Languages< /answer>
        < answer>Second Generation Languages< /answer>
        < answer>Third Generation Languages< /answer>
        < answer>Fourth Generation Languages< /answer>
        < correct>2< /correct>
      < /question>

      < question>
        < quizquestion>Which is the default package that is automatically visible to your program ?< /quizquestion>
        < answer>java.net< /answer>
        < answer>javax.swing< /answer>
        < answer>java.io< /answer>
        < answer>java.lang< /answer>
        < correct>3< /correct>
      < /question>	 

     < question>
        < quizquestion>Which entry in WEB-INF is used to map a servlet ?< /quizquestion>
        < answer>servlet-mapping< /answer>
        < answer>servlet-registration< /answer>
        < answer>servlet-entry< /answer>
        < answer>servlet-attachment< /answer>
        < correct>0< /correct>
      < /question>	

     < question>
        < quizquestion>What is the length of Java datatype int ?< /quizquestion>
        < answer>32 bit< /answer>
        < answer>16 bit< /answer>
        < answer>64 bit< /answer>
        < answer>Runtime specific< /answer>
        < correct>0< /correct>
      < /question>	

     < question>
        < quizquestion>What is the default value of Java datatype boolean?< /quizquestion>
        < answer>true< /answer>
        < answer>false< /answer>
        < answer>1< /answer>
        < answer>0< /answer>
        < correct>1< /correct>
      < /question>	 	   

    < /questions>
< /quiz>
```

## 开始新检查时设置计时器

当用户开始新的考试时，我们将用户会话中测验的总问题数和持续时间设置为一个属性。

```
request.getSession().setAttribute("totalNumberOfQuizQuestions",document.getElementsByTagName("totalQuizQuestions").item(0).getTextContent());
				request.getSession().setAttribute("quizDuration",document.getElementsByTagName("quizDuration").item(0).getTextContent());
				request.getSession().setAttribute("min",document.getElementsByTagName("quizDuration").item(0).getTextContent());
				request.getSession().setAttribute("sec",0);
```

## 倒计时时间

我们必须在每秒钟后递减计时器，为此，我们将创建一个 Javascript 函数，它将在考试页面加载时首次被调用，然后我们将在每秒钟后递归调用该函数以倒计时。

**Javascript 函数倒计时时间**

```
< script language ="javascript" >
        var tim;       
        var min = '${sessionScope.min}';
        var sec = '${sessionScope.sec}';
        var f = new Date();

        function customSubmit(someValue){  
        	 document.questionForm.minute.value = min;   
        	 document.questionForm.second.value = sec; 
        	 document.questionForm.submit();  
        	 }  

        function examTimer() {
            if (parseInt(sec) >0) {

			    document.getElementById("showtime").innerHTML = "Time Remaining :"+min+" Minutes ," + sec+" Seconds";
                sec = parseInt(sec) - 1;                
                tim = setTimeout("examTimer()", 1000);
            }
            else {

			    if (parseInt(min)==0 && parseInt(sec)==0){
			    	document.getElementById("showtime").innerHTML = "Time Remaining :"+min+" Minutes ," + sec+" Seconds";
				     alert("Time Up");
				     document.questionForm.minute.value=0;
				     document.questionForm.second.value=0;
				     document.questionForm.submit();

			     }

                if (parseInt(sec) == 0) {				
				    document.getElementById("showtime").innerHTML = "Time Remaining :"+min+" Minutes ," + sec+" Seconds";					
                    min = parseInt(min) - 1;
					sec=59;
                    tim = setTimeout("examTimer()", 1000);
                }

            }
        }
    < /script>
```

## 如何调用 Javascript 函数

现在，为了调用这个 Javascript 函数，我们将使用 body 标签的 onload 属性。

```
< body onload=”examTimer”>
```

## 向考试管理员提交考试时间

到目前为止，我们将测验问题表单直接提交给考试控制器，但现在我们必须发送计时器参数:分钟和秒钟，这样当考试控制器显示下一个问题时，它也应该显示正确的剩余时间。为此，我们使用 Javascript 手动提交表单，并将 min 和 sec 参数发送给考试控制器。

## 使用 Javascript 提交表单

请注意，当用户单击“下一步”、“上一步”或“完成”按钮时，将调用 customSubmit() Javascript 函数。

```
< form action="exam" method="post" name="questionForm" >
 < c:forEach var="choice" items="${sessionScope.quest.questionOptions}" varStatus="counter">
 < input type="radio" name="answer" value="${counter.count}" >${choice}  < br/>
 < /c:forEach> < br/> 

 < c:if test="${sessionScope.quest.questionNumber > 0}">
 < input type="submit" name="action" value="Previous" onclick="customSubmit()" />
 < /c:if>

 < c:if test="${sessionScope.quest.questionNumber <  sessionScope.totalNumberOfQuizQuestions-1}">
 < input type="submit" name="action" value="Next" onclick="customSubmit()" />
 < /c:if> 

 < input type="submit" name="action" value="Finish Exam" onclick="customSubmit()" />

< input type="hidden" name="minute"/> 
< input type="hidden" name="second"/>

< /form>
```

**customSubmit()函数**

将分钟和秒钟参数发送给 ExamController 的是 customSubmit()函数。

```
  function customSubmit(someValue){  
        	 document.questionForm.minute.value = min;   
        	 document.questionForm.second.value = sec; 
        	 document.questionForm.submit();  
        	 }
```

## 更新用户会话中的倒计时定时器

我们检索发送给 ExamController 的分钟和秒钟参数值，并在用户会话中更新它。

```
if(request.getParameter("minute")!=null)
			{			
			minute=Integer.parseInt(request.getParameter("minute"));
			second=Integer.parseInt(request.getParameter("second"));
			request.getSession().setAttribute("min",request.getParameter("minute") );
			request.getSession().setAttribute("sec",request.getParameter("second") );
			}
```

## 处理时间到了

当测验结束时，换句话说，当分和秒都变为零时。我们显示一个警告框，提示“时间到了”，并将分钟和秒钟的值设置为零，然后提交表单。

```
  if (parseInt(min)==0 && parseInt(sec)==0){
			    	document.getElementById("showtime").innerHTML = "Time Remaining :"+min+" Minutes ," + sec+" Seconds";
				     alert("Time Up");
				     document.questionForm.minute.value=0;
				     document.questionForm.second.value=0;
				     document.questionForm.submit();

			     }
```

我们必须更改代码，以便在考试时限结束时完成考试。

```
else if("Finish Exam".equals(action)||( minute==0 && second==0))
			{   finish=true;
				int result=exam.calculateResult(exam);				
				request.setAttribute("result",result);
				request.getSession().setAttribute("currentExam",null);
				request.getRequestDispatcher("/WEB-INF/jsps/result.jsp").forward(request,response);

			}
```

因此，可以通过直接单击“完成”按钮或在考试时限结束时(分和秒都变为零)结束考试。

这个帖子到此为止。在下一篇文章中，我们将进一步扩展我们的测验应用程序并添加新功能，以便用户能够查看自己的答案，并知道哪些问题是错的，哪些是正确的答案。要了解更多信息，请立即查看此[全栈开发人员课程](https://www.edureka.co/masters-program/full-stack-developer-training)。

像往常一样，你可以下载代码，随心所欲地修改它。这是理解代码的最佳方式。如果您有任何问题或要求，请在下面评论。

单击下载按钮下载代码。

有问题要问我们吗？请在评论区提到它，我们会给你回复。

**相关帖子:**

[Java 入门/J2EE](https://www.edureka.co/java-j2ee-soa-training "Get started with Java/J2EE and SOA")

[使用 JSP Servlet 创建在线测验应用程序](https://www.edureka.co/blog/creating-an-online-quiz-application-using-jsp-servlet/ "Creating an online quiz application using JSP servlet")