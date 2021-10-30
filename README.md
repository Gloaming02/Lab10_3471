Name: Zhengyan Hu

Tasks to answer in your own README.md that you submit on Canvas:

1.  See logger.log, why is it different from the log to console?
Because all test go through the logger.log together. They will go through the console one by one. 

2.  Where does this line come from? FINER org.junit.jupiter.engine.execution.ConditionEvaluator logResult Evaluation of condition [org.junit.jupiter.engine.extension.DisabledCondition] resulted in: ConditionEvaluationResult [enabled = true, reason = '@Disabled is not present']
It come from ConditionEvaluationResult. because Disabled is not present.

3.  What does Assertions.assertThrows do?
It will catch the exception we want to throw in the test. 

4.  See TimerException and there are 3 questions
    1.  What is serialVersionUID and why do we need it? (please read on Internet)
	SerialVersionUID is a unique identifier for each class, JVM uses it to compare the 	versions of the class ensuring that the same class was used during Serialization 	is loaded during Deserialization. 

    2.  Why do we need to override constructors?
	In this way we can throw with a message and cause.

    3.  Why we did not override other Exception methods?
	because we don't need to use other Exception methods in this assignment.
	
5.  The Timer.java has a static block static {}, what does it do? (determine when called by debugger)
The code in the block is run once for each time a class is loaded into memory.

6.  What is README.md file format how is it related to bitbucket? (https://confluence.atlassian.com/bitbucketserver/markdown-syntax-guide-776639995.html)
README.md files are Markdown files that describe a directory. Bitbucket uses CodeMirror to apply syntax highlighting to the rendered markdown in comments, READMEs and pull request descriptions.

7.  Why is the test failing? what do we need to change in Timer? (fix that all tests pass and describe the issue)
Because the function is throw a null pointer exception instead of timer exception. I change the timeNow to initialize to System.currentTimeMillis() instead of null. Because long can't be null. That why the null pointer exception throw.

8.  What is the actual issue here, what is the sequence of Exceptions and handlers (debug)
Because the program throws 2 exception the first one is null pointer exception throw by long. The second one is the timer exception we throw in the condition of timeToWait<0. So when we throw, the system will first throw the null pointer exception.

9.  Make a printScreen of your eclipse JUnit5 plugin run (JUnit window at the bottom panel) 
10.  Make a printScreen of your eclipse Maven test run, with console
11.  What category of Exceptions is TimerException and what is NullPointerException
Exceptions is runtime exception. Null Pointer exception is also runtime. It will check any null value of object.

12.  Push the updated/fixed source code to your own repository.
