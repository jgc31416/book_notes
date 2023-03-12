
## Findings ##

The gap from high performers to low performers is widening, the devops mantra of continuous improvement makes them pull from medium performers.

There are a few characteristics that high performers share:
- On demand deployment
- Less than one hour for a change to be deployed.
- Change failure rate of 0-15%
- Mean time to restore: less than 1 hour.

Strategic software delivery performance affects organizational performance

## Culture

Devops influences culture.
- Assumptions: interpretation of rules derived from interactions, they are not visible.
- Values: collective ideas that can be shared and discussed, allows interpretation and provide context.
- Artifacts: these are procedures and rituals.

## Westrum model

- Pathological-> power oriented. Failure leads to scape goats.
- Burocratic, where failure leads to justice.
- Generative -> focused on the mission, there is more cooperation, training and bridging attitudes are fostered. Failure leads to enquiry.

This model is a continuous, companies can be measured, tests do exist to figure out where you stand.

The model mainly affects how information is shared and processed.
Sharing information should level the playing field and increase the trust between the staff. 


## Continuous delivery ##

This is a set of capabilities that allows teams to get changes of all kinds in production safely, quickly and sustainably. There capabilities are:
- Quality built in.
- Work in small batches to allow fast feedback, from the PR review to the customer's feedback.
- Computers perform repetitive tasks, people solve problems.
- Ralentlessly pursue continuous improvement.
- Everyone is responsible.

Foundations:
- Comprehensive configuration management. Any change to the environment where the sw runs should be under version control.
- Continuous integration, there is continous emphasys on doing short lived branches or even trunk base development.
- Continuous testing: 
	- Test should be reliable and built by by developers.
	- Test data should be available.
	

The practice of CD seems to be associated to stronger identification with the organization you work for and the generative culture.

## Architecture ##

High performance is possible in all kind of systems, from web apps to mainframe.

Loose coupling seems the key characteristic in the architecture that allows for high performance, in conjunction with:
- Testing without an integrated environment.
- Independently deployable, the team can deploy its sw without breaking other systems, and without the acceptance or syncronization with other teams.

Loose coupling allows for scaling, meaning that we can keep growing the engineering teams while keeping productivity.

**Allow teams to choose their own tools** 
Usually the engineers can find the best tools to solve their team's problems. Said that, there seems to be benefits on standardization around architecture and configuration of infrastructure, specially improving operations.

**Architects should focus on engineers and outcomes**
The main mission should be to support engineers to achieve better outcomes

## Integrating InfoSec ##

Shift left improves delivery performance by limiting the work to fix security issues.
Security in the loop should make sure that security tests are integrated from the beginning of the project, its feedback and education should be present.

Retrofitting security can be very expensive, high performers spend 50% less dealing with security issues.

There is a reference to the rugged manifesto, I guess that the most important point is that you should think like a hacker when building systems, try to find loopholes and cracks, and fix them before releasing. Assume that the code can be under attack, and can live for years to come.


## Lean management ##

- Limit the work in progress
- Visual management
- Feedback from production
When combined together they provide a strong predictor for high performance teams, just by themselves not that much. Limiting the WIP should help give obstacles visibility.

- Lightweight change approvals
Seems that change approvals by peer review is the most effective change management. 
External approval is just waste.


## Product development ##

Some of the practices linked to high performing companies studied:
- Slice features to 1 week implementables.
- Flow from the business to the user perfectly visible.
- Active andn regularly seek customer feedback.
- Development can change specifications without approval.

Work in small batches allow to integrate the results of the research in the product.


## Deployment pain ##

A synonym of fear and anxiety felt when releasing a new version, the objective is to minimize it. These problems are correlated with poor IT and organizational performance.

Then the book makes an association between deployment pain and burnout that seems to me a bit far reached. 
Lean practices seams to lead to less burnout.

## Employee satisfaction ##

Measured by the Net Promoter Score, not sure about this chapter.
One of the key contributors to burnout is misalignment between personal and organizational values.
People feel better when they see the benefits to the customer, lean management should improve the situation on this regard.
There is a call to diversify the workforce, always useful. 


## Leadership ##

Its main functions are:
- Establish and support generative and high trust cultural norms.
- Support team experimentation and innovation.
- Work across organizational silos to achieve strategic alignment.

There are a set of characteristics for transformational leadership:
- Vision.
- Inspirational communication.
- Intellectual stimulation.
- Supportive leadership.
- Personal recognition.

How the leadership mark against these characteristics is related to the performance of the team, however you can still find good leadership in low performing teams, so it is not enough.

Activities that help creating a learning/improvement climate
- Create a training budget and make it actionable.
- Ensure resources to engage in exploratory work.
- Create hack days where cross functional teams get together.
- Make it safe to fail.
- Create opportunities and spaces to share information, demo days, forums, weekly lighning talks and so on.


