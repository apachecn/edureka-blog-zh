# 使用 JSP Servlet 创建在线测验应用程序

> 原文：<https://www.edureka.co/blog/creating-an-online-quiz-application-using-jsp-servlet/>

在本帖中，我们将介绍使用 JSP Servlet 技术创建交互式在线测验应用程序的步骤。我们将了解如何解析 XML 文件，如何处理会话，以及如何使用会话管理跟踪用户交互。

## 创建在线测验应用程序

以下是终端应用的一些快照:

## 注册页面

在参加测验之前，用户必须首先注册并登录。要注册，可以直接点击注册菜单或登录页面上提供的注册页面链接来创建帐户。

## 登录页面

当用户单击时，如果用户未登录，考试用户将被直接重定向到登录页面。

[![Login Page](img/6ec93706b61bfe77ea796aecad119a24.png "Login Page")](https://cdn.edureka.co/blog/wp-content/uploads/2015/01/Login-Screen.png)

## 用户主页

主页是应用程序的登录页面，用户可以在这里通过单击测验进行任何测验。在主页上，如果用户已登录，还会显示其姓名，并提供一个注销链接，用于从应用程序中注销。

## [![Home Page](img/a8ba0b95bf57580ab7f8210428a816cd.png "Home Page")](https://cdn.edureka.co/blog/wp-content/uploads/2015/01/Home-Screen.png)

## 测验屏幕

开始测验时，会向用户显示测验的第一个问题，并显示“下一个”和“完成”按钮。注意，当用户在第一个问题上时，不显示“上一步”按钮，当用户在最后一个问题上时，不显示“下一步”按钮。

[![Quiz Screen](img/7fb46e30a1480093872b4e710fb1eeb1.png "Quiz Screen")](https://cdn.edureka.co/blog/wp-content/uploads/2015/01/QuestionScreen.png)

[![Quiz Screen](img/b40847830fb5ff4109172c89890fdbe4.png "Quiz Screen")](https://cdn.edureka.co/blog/wp-content/uploads/2015/01/QuestionScreen-2.png)

## 测验结果

点击完成按钮后，用户将看到考试结果，显示测验的名称；测验开始的时间以及用户答对的问题数。

[![Quiz Result](img/83e703667c929d16f8f97f8908194560.png "Quiz Result")](https://cdn.edureka.co/blog/wp-content/uploads/2015/01/Result-Screen.png)

## 这个测验应用程序是如何工作的？

嗯，它按照你期望的那样工作。要参加测验，用户必须登录。如果用户没有登录，用户将被自动重定向到登录页面，用户可以在此登录。如果用户还没有注册到应用程序，他必须首先创建一个帐户。成功登录应用程序后，用户可以通过单击它来参加任何测验。现在，将向用户展示测验的第一个问题。为了浏览测验问题，为用户提供了“下一个”和“上一个”按钮。单击“完成”按钮，可以随时结束测验。

让我们开始构建应用程序

下面是 Eclipse IDE 中项目结构的快照。

## 项目结构

[![Eclipse Project Structure](img/3337bf9806a344262bc75f8f88c68212.png "Eclipse Project Structure")](https://cdn.edureka.co/blog/wp-content/uploads/2015/01/Project_Structure1.png)

## 创建主页

主页非常简单。我们有一个菜单和 8 个图像，以两行表格格式显示；每行包含 4 幅图像。在主页上，我们还会检查用户是否登录。如果用户已经登录，我们还会显示用户名并提供一个注销链接。

**创建主页菜单**

```
< div id='cssmenu'>
< ul>
   < li class=''>< a href='${pageContext.request.contextPath}'>< span>Home< /span>< /a>< /li>
   < li>< a href='${pageContext.request.contextPath}/login'>< span>Login< /span>< /a>< /li>
   < li>< a href='${pageContext.request.contextPath}/register'>< span>Register< /span>< /a>< /li>
   < li class='#'>< a href='#'>< span>Submit a Question< /span>< /a>< /li>
   < li class='#'>< a href='#'>< span>Feedback< /span>< /a>< /li>
   < li>< a href='#'>< span>Contribute< /span>< /a>< /li>
   < li>< a href='#'>< span>Contact us< /span>< /a>< /li>
< /ul>
< /div>

```

**检查用户是否登录**

```
< c:if test='${not empty sessionScope.user}'>

< div style="position:absolute;top:70px;left:1100px">
Logged as < a href="#" class="button username">${sessionScope.user}< /a>
< /div>

< div style="position:absolute;top:70px;left:1300px">
< a href='${pageContext.request.contextPath}/logout'>Logout< /a>
< /div>

< /c:if>
```

**在主页上显示测验图像**

```
< div style="position:absolute;left:120px;top:60px">
< table cellpadding="0" cellspacing="50">

< tr>
< td>< a href="takeExam?test=java">< img height="200" width="200" src="${pageContext.request.contextPatimg/java.png"/>< /a>< /td>
< td>< a href="takeExam?test=javascript">< img height="200" width="200" src="${pageContext.request.contextPatimg/javascript.png"/>< /a>< /td>
< td>< a href="takeExam?test=sql">< img height="200" width="200" src="${pageContext.request.contextPatimg/sql-logo.png"/>< /a>< /td>
< td>< a href="takeExam?test=python">< img height="200" width="200" src="${pageContext.request.contextPatimg/python.jpg"/>< /a>< /td>
< /tr>

< tr>
< td>< a href="takeExam?test=css">< img height="200" width="200" src="${pageContext.request.contextPatimg/css.jpg"/>< /a>< /td>
< td>< a href="takeExam?test=php">< img height="200" width="200" src="${pageContext.request.contextPatimg/php-logo.jpg"/>< /a>< /td>
< td>< a href="takeExam?test=linux">< img height="200" width="200" src="${pageContext.request.contextPatimg/logo-linux.png"/>< /a>< /td>
< td>< a href="takeExam?test=mongodb">< img height="200" width="200" src="${pageContext.request.contextPatimg/mongodb_logo.png"/>< /a>< /td>
< /tr>

< /table>
< /div>
```

## 创建用户注册页面

注册页面没有什么花哨的；只是一个 HTML 表单，等待用户提供他的名字，电子邮件和密码。一旦我们得到它，我们就把它传递给 RegistrationController servlet 来创建一个帐户。

注意:我们不做任何验证，如密码应包含 8 个字符，至少有一个大写字符，一个数字和特殊符号。当我们扩展这个应用程序时，我们将在以后的文章中这样做。

**注册码**

```
protected void doPost(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {		
		String username=request.getParameter("username");
		String email=request.getParameter("email");
		String password=request.getParameter("password");

		Connection con=DatabaseConnectionFactory.createConnection();

		try
		{
		 Statement st=con.createStatement();
		 String sql = "INSERT INTO users values ('"+username+"','"+password+"','"+email+"')";
		 		System.out.println(sql);
		 st.executeUpdate(sql);
		}catch(SQLException sqe){System.out.println("Error : While Inserting record in database");}
		try
		{
		 con.close();	
		}catch(SQLException se){System.out.println("Error : While Closing Connection");}
        request.setAttribute("newUser",username);
		RequestDispatcher dispatcher=request.getRequestDispatcher("/WEB-INF/jsps/regSuccess.jsp");
		dispatcher.forward(request, response);		
	}
```

## 获取数据库连接

在这个应用程序中，我们使用 MySQL 数据库来存储用户凭证。为了连接到数据库，我们在 DatabaseConnectionFactory 类中定义了一个静态方法 createConnection，其中存储了所有数据库特定的信息。

我们只有测验数据库下的用户表。

**用户表**

```
create table users(username varchar(50),email varchar(50),password varchar(50))
```

如果您正在使用 Oracle 等其他数据库，则必须相应地更改 DatabaseConnectionFactory 类的属性。

**DatabaseConnectionFactory.java**

```
public class DatabaseConnectionFactory {

	private static String dbURL="jdbc:mysql://localhost/quiz";
	private static String dbUser="root";
	private static String dbPassword="";

	public static Connection createConnection()
	{
		 Connection con=null;
		try{
			try {
				   Class.forName("com.mysql.jdbc.Driver");
				}
				catch(ClassNotFoundException ex) {
				   System.out.println("Error: unable to load driver class!");
				   System.exit(1);
				}			
		     con = DriverManager.getConnection(dbURL,dbUser,dbPassword);
		   }
		  catch(SQLException sqe){ System.out.println("Error: While Creating connection to database");sqe.printStackTrace();}
		return con;
	}

}
```

## 创建登录页面

登录页面非常类似于注册页面，我们提供两个输入字段，要求用户提供用户名和密码。一旦我们得到用户输入的用户名和密码，我们就把它传递给 LoginController 来验证用户。

**登录验证码**

```
protected void doPost(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {

		String username=request.getParameter("username");
		String password=request.getParameter("password");				
		Connection con=DatabaseConnectionFactory.createConnection();		
		ResultSet set=null;
		int i=0;
		try
		{
		 Statement st=con.createStatement();
		 String sql = "Select * from  users where username='"+username+"' and password='"+password+"' ";
		 		System.out.println(sql);
		 set=st.executeQuery(sql);
		 while(set.next())
		 {
			 i=1;
		 }
		 if(i!=0)
		 {   HttpSession session=request.getSession();
		     session.setAttribute("user",username);
			 RequestDispatcher rd=request.getRequestDispatcher("/WEB-INF/jsps/home.jsp");
			 rd.forward(request, response);

		 }
		 else
		 {   request.setAttribute("errorMessage","Invalid username or password");
			 RequestDispatcher rd=request.getRequestDispatcher("/WEB-INF/jsps/login.jsp");
			 rd.forward(request, response);
		 }
		}catch(SQLException sqe){System.out.println("Error : While Fetching records from database");}
		try
		{
		 con.close();	
		}catch(SQLException se){System.out.println("Error : While Closing Connection");}
	}
```

## 应用程序的主控制器

这是主控制器，我们在其中编写了代码，根据传入的请求 url 将用户重定向到适当的页面。

```
@WebServlet(urlPatterns = { "/login", "/register", "/takeExam", "/logout" })
public class MainController extends HttpServlet {
	private static final long serialVersionUID = 1L;

	protected void doGet(HttpServletRequest request,
			HttpServletResponse response) throws ServletException, IOException {

		String applicationContextPath = request.getContextPath();

		if (request.getRequestURI().equals(applicationContextPath + "/")) {
			RequestDispatcher dispatcher = request
					.getRequestDispatcher("/WEB-INF/jsps/home.jsp");
			dispatcher.forward(request, response);
		} else if (request.getRequestURI().equals(
				applicationContextPath + "/login")) {
			RequestDispatcher dispatcher = request
					.getRequestDispatcher("/WEB-INF/jsps/login.jsp");
			dispatcher.forward(request, response);
		} else if (request.getRequestURI().equals(
				applicationContextPath + "/register")) {
			RequestDispatcher dispatcher = request
					.getRequestDispatcher("/WEB-INF/jsps/register.jsp");
			dispatcher.forward(request, response);
		} else if (request.getRequestURI().equals(
				applicationContextPath + "/takeExam")) {
			request.getSession().setAttribute("currentExam", null);

			String exam = request.getParameter("test");
			request.getSession().setAttribute("exam", exam);

			System.out.println(request.getSession().getAttribute("user"));
			if (request.getSession().getAttribute("user") == null) {
				request.getRequestDispatcher("/login").forward(request,
						response);

			} else {
				RequestDispatcher dispatcher = request
						.getRequestDispatcher("/WEB-INF/jsps/quizDetails.jsp");
				dispatcher.forward(request, response);
			}
		} else if (request.getRequestURI().equals(
				applicationContextPath + "/logout")) {
			request.getSession().invalidate();
			RequestDispatcher dispatcher = request
					.getRequestDispatcher("/WEB-INF/jsps/home.jsp");
			dispatcher.forward(request, response);
		}

	}

}
```

## 实现注销功能

一旦用户单击注销，链接会话就会失效，会话中绑定的所有对象都会被删除。

```
request.getSession().invalidate();
```

## 存储测验问题

请注意，我们将问题存储在单独的 XML 文件中，而不是数据库中。

```
< quiz>
  < title>MongoDB Quiz (01/09/2015)< /title>
    < questions>    
      < question>
        < quizquestion>MongoDB is a < /quizquestion>
        < answer>Relational Database< /answer>
        < answer>Object Relational Database< /answer>
        < answer>Graph Database< /answer>
        < answer>Document Database< /answer>
        < correct>3< /correct>
      < /question>

      < question>
        < quizquestion>What is the name of MongoDB server ?< /quizquestion>
        < answer>mongoserver< /answer>
        < answer>mongod< /answer>
        < answer>mongodb< /answer>
        < answer>mongo< /answer>
        < correct>1< /correct>
      < /question>

      < question>
        < quizquestion>What is the name of MongoDB client ?< /quizquestion>
        < answer>mongo< /answer>
        < answer>mongod< /answer>
        < answer>mongodb< /answer>
        < answer>mongo-client< /answer>
        < correct>0< /correct>
      < /question>
< /questions>
< /quiz>
```

## 如何读取 XML 文件中存储的问题

为了从 XML 文件中读取问题，我们创建了一个表示包含测验问题的 XML 文件的文档。每当用户点击下一个或上一个按钮时，我们调用 setQuestion(int i)方法，给出我们想要读取的问题的索引，同时该问题保存在 QuizQuestion 的 ArrayList 中。

## 如何表示一个问题？

QuizQuestion 是表示单个测验问题的类；每个问题将有一个数字，问题陈述，选项和一个正确的选项索引。

**QuizQuestion.java**

```
public class QuizQuestion {

	int questionNumber;
	String question;
	String questionOptions[];
	int correctOptionIndex;

	public String getQuestion()
	{ 
		return question;
	}

	public int getQuestionNumber()
	{
		return questionNumber;
	}

	public void setQuestionNumber(int i)
	{
		questionNumber=i;
	}

	public int getCorrectOptionIndex()
	{
		return correctOptionIndex;
	}

	public String[] getQuestionOptions()
	{
		return questionOptions;
	}

	public void setQuestion(String s)
	{
		question=s;
	}
	public void setCorrectOptionIndex(int i)
	{
		correctOptionIndex=i;
	}
	public void setQuestionOptions(String[]s)
	{
		questionOptions=s;
	}

}
```

请注意，由于这是一个 web 应用程序，多个用户将同时参加考试。我们必须确保一个用户的考试不会影响到另一个用户的考试。例如，一个用户可能刚刚开始 Java 考试，而另一个用户正在进行 SQL 考试的问题 5；我们必须将它们视为两个独立的考试。为此，我们将使用 session 维护每个考试的状态。

当用户点击开始考试按钮开始考试时，我们将创建一个新的考试实例，通过测试类型，如 Java，PHP，CSS 等。因此每个用户都有一个不同的 Exam 类实例(代表一个单独的考试)。

让我们看看考试课有什么

```
public class Exam {
	Document dom;
	public int currentQuestion=0;	

	public Map selections=new LinkedHashMap();
	public ArrayList questionList = new ArrayList(10);

	public Exam(String test) throws SAXException,ParserConfigurationException,IOException, URISyntaxException{
		dom=CreateDOM.getDOM(test);
	}

      // code
}
```

注意，为了跟踪考试中的当前问题，我们在考试类中有 current question 属性。

## 处理整个考试

ExamController 是我们控制考试的主要控件。在这里，我们将用户选择(用户对问题的回答)保存在地图中。ExamController 还允许用户通过单击下一个和上一个按钮来浏览问题，在后端，是 ExamController 进行函数调用来检索问题并存储用户响应。

## 提交考试并评估考试结果

当用户单击“完成”按钮时，ExamController 调用 calculateResult()方法传递考试对象，calculateResult()将用户响应与问题的正确选项进行比较，并返回用户得到了多少个正确答案。

```
public int calculateResult(Exam exam){
		int totalCorrect=0;
		Map<Integer,Integer> userSelectionsMap=exam.selections;		
		List userSelectionsList=new ArrayList(10);
		for (Map.Entry<Integer, Integer> entry :userSelectionsMap.entrySet()) {
			userSelectionsList.add(entry.getValue());
		}
		List questionList=exam.questionList;
		List correctAnswersList=new ArrayList(10);
		for(QuizQuestion question: questionList){
			correctAnswersList.add(question.getCorrectOptionIndex());
		}

		for(int i=0;i<selections.size();i++){
			System.out.println(userSelectionsList.get(i)+" --- "+correctAnswersList.get(i));
			if((userSelectionsList.get(i)-1)==correctAnswersList.get(i)){
				totalCorrect++;
			}
		}

		System.out.println("You Got "+totalCorrect+" Correct");	
		return totalCorrect;
	}
```

请注意，到目前为止，我们的每个问题都有 4 个选项，测验没有计时器。在即将发布的帖子中，我们将扩展这个在线测验应用程序，并将包括以下功能:

1.每个测验可以有不同数量的问题

2.每个问题可以有不同数量的选项

3.一个问题可以有多个正确选项

4.为测验实现计时器

5.维护用户的历史；比如用户过去参加了多少次测试以及他的分数

6.随机化呈现给用户的问题的顺序

7.给予用户在提交测试进行评估之前检查其答案的选项

8.一个下拉框，跳转到测试之间的任何问题，而不是点击下一步按钮多次。

像往常一样，你可以下载代码，随心所欲地修改它。这是理解代码的最佳方式。如果您有任何问题或建议，请在下面评论。

单击下载按钮下载代码。

【button leads form _ title = " Download Code " redirect _ URL = https://edu reka . wistia . com/medias/akdu 7 ycjex/Download？media _ file _ id = 65416744 course _ id = 44 button _ text = "下载代码"]

有问题要问我们吗？请在评论区提到它，我们会给你回复。

**相关帖子:**

[创建在线测验应用程序第 2 部分——实现倒计时定时器](https://www.edureka.co/blog/creating-an-online-quiz-application-implementing-countdown-timer/)

[创建在线测验应用程序第 3 部分——测验复习功能](https://www.edureka.co/blog/online-quiz-application-quiz-review/)

[Java 入门/J2EE](https://www.edureka.co/java-j2ee-soa-training)

[和 Edureka 一起揭开 Java 课程的神奇！](https://www.edureka.co/blog/java-tutorial)