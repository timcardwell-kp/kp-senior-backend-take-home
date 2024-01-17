## What do I need to submit?

Please write a .NET Web API that implements a *Survey* service. We must be able to run your solution. Provide any documentation necessary to accomplish this as part of the repository you submit.
## What does it need to do?

### Background

You are building a service for managing surveys and survey results. A survey is a form, created by a user, with a series of questions on it. A survey result is the submission of an existing survey by a user.

For example:
```csharp
public class Survey
{
	public Guid Id;
	public string Name;
	public List<Question> Questions;
}

public class Question
{
  public Guid Id;
  public string Description;
}
```

Additionally, a survey must be activated before it can receive submissions. Once activated, all surveys are only valid for 24 hours.
### What we expect your service to do

Create the following API endpoints:
- CreateSurvey
- ActivateSurvey
- CreateFormSubmission

Additionally, there are events that need to be communicated to other services external to the one you are building. These events are:
- SurveyActivated
- FormSubmissionCreated

Be sure to include things like model validation and business validation (such as the 24 hour time limit for a survey) in your code.

While we are looking for overall correctness of your service, you should build this service as if it were eventually going to be running in production, being maintained by a team of engineers. This means you should be following accepted software engineering standards, such as SOLID principles. 

Feel free to add in other patterns, strategies, and packages for managing software complexity that you feel could be beneficial to include in a microservice running in an enterprise suite of services.
### What we do not expect your service to do
- You do not need to integrate with a database, but be sure to at least mock out classes that may be responsible for data access.
- You do not need to integrate with an enterprise service bus, or other messaging provider, but be sure to at least mock out classes that may be responsible for these actions
- You do not need to worry about authentication or authorization
## How do I submit it?

Provide us with a link to a public GitHub repository that contains your code.
