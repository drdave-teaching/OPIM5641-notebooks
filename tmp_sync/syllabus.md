# OPIM 5641: Business Decision Modeling

# Syllabus — Fall 2026

> Markdown master. The `.docx` in this folder is regenerated from this file — edit here first. If they ever disagree, the docx submitted to the department wins.

**Excluding materials for purchase, syllabus information may be subject to change. The most up-to-date syllabus is located within the course in HuskyCT.**

## Course and Instructor Information

- **Course Title:** OPIM 5641: Business Decision Modeling
- **Credits:** 3
- **Format:** Hybrid — seven in-person studios in **Stamford** on alternating **Wednesdays, 5:30–7:30 PM**, with asynchronous video modules in the weeks between. Week 1 (September 2) is asynchronous; our **first in-person studio is Wednesday, September 9**.
- **Prerequisites:** None.
- **Professor:** Dave Wanik
- **Email:** [dave.wanik@uconn.edu](mailto:dave.wanik@uconn.edu)
- **Grader:** Anushka Rajoriya — [jwa25001@uconn.edu](mailto:jwa25001@uconn.edu)
- **Office Hours/Availability:** **Fridays at 12:00 PM (noon) on Microsoft Teams.** [Join the Teams meeting](https://teams.microsoft.com/meet/293846509548835?p=021uy603QFo2YsIj5Q) · Meeting ID: 293 846 509 548 835 · Passcode: At2KV2w8 · Dial in: +1 475-282-1761, code 863068052#. I will try to respond to email questions within 24 hours. I will also monitor the discussion board at least once per day for questions. I will not reply to emails re: assignments/group project work 24 hours before the due date. Grades will typically be posted within ten days.

## How This Hybrid Course Works

This course alternates every other week between an in-person studio in Stamford and an asynchronous week you complete on your own schedule.

**Async weeks:** short videos (typically 5–10 minutes each) walk you through the notebooks, which all run in Google Colab — nothing to install. You watch, you run the code yourself, and you upload that week's handwritten math check. Everything is posted in HuskyCT, organized by module.

**Studio weeks:** we meet in Stamford for two hours. Studios are not lectures — the lecture already happened on video. We open with the handwritten math check, then formulate a fresh business case together, solve it by hand, build it live in Pyomo, and finish with time on your final project.

The pattern matters: async is where you learn the mechanics at your own pace with a pause button, and studio is where you apply them on messy problems with a person in the room. Come to studio having watched the videos.

## Course Materials

**Main Textbook:**

- "Business Analytics: The Art of Modeling With Spreadsheets, 5th Edition" — Stephen G. Powell, Kenneth R. Baker — ISBN: 978-1-119-29842-7
  - Although this book uses Excel and Solver, we will solve all examples using Python instead. Not required but useful if you need more background on optimization topics (try to get a used copy or PDF).

**Optional Textbooks:**

- Managerial Decision Modeling with Spreadsheets, Third Edition. Nagraj Balakrishnan, Barry Render, Ralph M. Stair, Jr. (especially Chapter 2 on graphical method)
- 'Introduction to Operations Research', Eleventh Edition. Hillier and Lieberman. (especially Chapters 1–4 on LP and simplex)
- Jeffrey Kantor's Pyomo Cookbook (free)
  - <https://jckantor.github.io/ND-Pyomo-Cookbook/>

Additional course readings and media are available within HuskyCT. Many books are available free-of-charge from the UConn Library — lib.uconn.edu.

**Required Materials:**

- **Second Monitor**, or tablet, desktop, laptop, etc.
  - This is important, so you can watch the videos and code at the same time. You will waste A LOT of time if you don't get a large, second screen.
- **Claude subscription** (Claude Pro, $20/month — [claude.ai](https://claude.ai))
  - We will use Claude throughout the course for the GenAI activities and for building agentic AI systems. Treat it like your textbook cost — this course has no textbook to buy.
- WebCam or built-in camera to say hello during office hours.

## Software/Technical Requirements (with Accessibility and Privacy Information)

The software/technical requirements for this course include:

- HuskyCT/Blackboard ([HuskyCT/Blackboard Accessibility Statement](http://www.blackboard.com/Platforms/Learn/Resources/Accessibility.aspx), [HuskyCT/Blackboard Privacy Policy](http://www.blackboard.com/footer/privacy-policy.aspx))
- [Adobe Acrobat Reader](http://www.adobe.com/products/acrobat/readstep2.html) ([Adobe Reader Accessibility Statement](http://www.adobe.com/accessibility/products/reader.html), [Adobe Reader Privacy Policy](http://www.adobe.com/privacy.html))
- Google Apps ([Google Apps Accessibility](https://www.google.com/accessibility/), [Google for Education Privacy Policy](https://www.google.com/edu/trust/))
- Microsoft Office and Microsoft Teams (free to UConn students through [uconn.onthehub.com](https://uconn.onthehub.com)) ([Microsoft Accessibility Statement](http://www.microsoft.com/enable/microsoft/mission.aspx), [Microsoft Privacy Statement](https://privacy.microsoft.com/en-us/privacystatement/))
- Dedicated access to high-speed internet with a minimum speed of 1.5 Mbps (4 Mbps or higher is recommended).

## Course Description

Discusses business modeling and decision analysis. Covers topics such as optimization, simulation, and sensitivity analysis to model and solve complex business problems. As **Python\*** is often used as a software tool for optimization, the course will emphasize developing high quality code to ensure that the objectives of the model are clear, defining the calculations, good design practices, testing and presenting the results.

\*This course will be taught using 100% Python! Studio 3 is a special-topics session with a guest speaker from industry.

## Course Objectives

By the end of the semester, students should be able to:

- Describe and analyze data using Python.
- Translate business problems into mathematical models (objective functions, decision variables, constraints.)
- Solve linear programming (allocation, covering, blending, network, integer) and nonlinear programming problems using Python.
- Perform sensitivity analysis and calculate shadow prices for binding constraints.
- Use Monte Carlo simulation to explore decision-making under uncertainty.
- Develop Python-based agentic AI systems that autonomously assist in formulating optimization and simulation models from business problem descriptions.
- Evaluate the effectiveness and limitations of agentic AI in supporting decision modeling and problem-solving.

## Course Outline and Objectives

**Module 1: Foundations — Exploratory Data Analysis and Monte Carlo**

- Develop well-designed Colab notebooks (organized layout, text cells with beautiful formatting; code cells with lots of comments)
- Describe, summarize and visualize data in Python
- Enrich existing data with external sources (like Wikipedia and Github)
- Implement Monte Carlo simulation and interpret the output probabilistically
- Explain when to explore data you have and when to simulate data you do not have
- **GenAI Activity:** Get set up with Claude ([claude.ai](https://claude.ai)) and create an Anthropic API key. Design, test, and refine an agentic AI system that parses a word problem into decision variables, constraints, and an objective function, and then generates Python code to solve the resulting optimization model.

**Module 2: Solving Linear Programs by Hand (Brute Force, Graphical Method, Simplex)**

- Solve optimization problems using the brute force method, and explain why it collapses as the problem grows
- Define the elements of a linear programming problem (objective function, decision variables, constraints) and solve 2D problems using the graphical method
- Solve 2D maximization problems using the Simplex algorithm: augmented form, the initial tableau, the minimum ratio test and pivoting to optimality (objective function in the BOTTOM row). Minimization by the dual and mixed constraints are not covered.
- **GenAI Activities:** Apply an agentic AI system to formulate and solve 2D linear programming problems using the graphical method, and verify the correctness of the AI's output. Use an agentic AI system to set up and solve linear programming problems with the Simplex algorithm, and evaluate the AI's reasoning and solutions against manual implementations.

**Module 3: Linear Programming in Pyomo (Allocation, Covering, Blending)**

- Translate narrative word problems into a basic mathematical formulation (build a mathematical representation of reality)
- Solve allocation (packing) and covering problems using Pyomo
- Convert proportions into linear constraints and solve blending problems
- Identify binding constraints and calculate shadow prices
- Perform sensitivity analysis transparently — vary the right-hand side in a loop and read the shadow price off the result
- **GenAI Activity:** Conduct sensitivity analysis with an agentic AI tool by generating and interpreting shadow prices, reduced costs, and RHS/objective-coefficient ranges, and explain the managerial implications of these results.

**Module 4: Nonlinear Optimization and Portfolios**

- Model a problem as a nonlinear optimization model and solve it using Pyomo. Separate model from data and use data structures to build constraints and calculations.
- Understand the difference between local and global optimal solutions, and apply techniques (initializing, bounding, multi-start) to improve your chances of finding the global optimum
- Cast regression as an optimization problem, and use real stock price data to allocate a portfolio for a given level of risk
- **GenAI Activity:** Enhance the stock portfolio optimization example by integrating real-time market data, scaling to larger asset sets, automating rebalancing, and producing multiple scenarios with plots using robust, soft-coded Python.

**Module 5: Integer Optimization**

- Change the domain of decision variables to force them to take on integer values
- Identify and define binary constraints and use them for project selection problems
- Identify and define fixed and variable costs, and use linking constraints to ensure consistency
- Use linking constraints to apply min/max thresholds and quantity discounts
- **GenAI Activity:** Create a dynamic work scheduling system for nurses, IT professionals or something else that is interesting to you.

**Module 6: Network Optimization**

- Conceptualize, draw and solve the transportation problem (where supply >= demand) for a minimum cost flow example
- Generalize the transportation model to a two-stage trans-shipment problem (requires a compound objective function)
- Solve shortest-path and assignment problems, and read the answer off a real map
- Apply Monte Carlo simulation techniques to network problems
- **GenAI Activity:** Scrape real-time data and build an agent that can distribute resources across a network, generating alternative scenarios and visualizations.

## Course Requirements and Grading

**Summary of Course Grading:**

| Course Components | Weight |
|---|---|
| Individual Assignments / GenAI Activities | 35% |
| Weekly Handwritten Math Checks | 25% |
| Studio Exercises (in class) | 10% |
| Final Project | 30% |

Students will be broken up into groups after Module 1 concludes — you will work with your groups on the final project, building it up in increments during the project block at the end of each studio. Groups will be balanced based on past coding experience as best we can.

**Individual Assignments and GenAI Activities**

Each module typically has one individual assignment. They are each worth 100 points and are graded for accuracy according to the rubric. These are the async-week deliverables — you build them from the videos and notebooks on your own time. GenAI activities may or may not be graded as part of individual assignments, as the primary goal is to enhance your coding skills and to help you build a data science portfolio.

**Group Projects**

Your group project is your chance to apply what you have learned in class to an interesting real-world problem that you would be proud talking about in a job interview. You will follow the same general flow for each project: data gathering, lit review, data preparation, modeling, analysis, conclusion, works cited/references. To keep things streamlined, ALL of your materials (code and text/narrative) can just be stored in the Colab notebook. Make sure your code is neat and organized (with lots of headers and comments). All students will be required to present on what they did for each project. We can't wait to see what you will do!

**Weekly Handwritten Math Checks**

There is no midterm. Instead there is a short (~15 minute) handwritten math check every week — descriptive statistics, corner points, one Simplex pivot, a 2-asset portfolio, a shortest path. On studio nights it is the warm-up when you walk in; on async weeks you work it on paper and upload a scan. Individually these are low stakes; together they are how you stay fluent. Your two lowest scores are dropped. Cramming Simplex once and forgetting it is exactly what we are trying to avoid — little and often beats big and once.

**Studio Exercises**

Each in-person studio includes a hands-on exercise done with your team — formulate a fresh business case, solve it by hand, then build and interpret the model live. These are graded for completion and good-faith effort rather than polish; the point is that you attempt the thinking in the room where you can ask questions. The studios are where this course does its real work, so please come. If you have to miss one, contact me in advance and I will give you the equivalent to do on your own.

**Grading Scale (per the Registrar): Graduate**

- The letter "A" represents work of distinction.
- The letter "B" represents work of good quality, such as is expected of any successful graduate student.
- The letter "C" represents work below the standard expected of graduate students in their area of study.
- The letter "D" represents work of unsatisfactory quality.
- The letters "F" and "U" signify failure in the course and necessitate a recommendation by the advisory committee to the Graduate School as to whether or not the student shall be permitted to continue graduate study.

Plus and minus values may be assigned to all but failing grades, are entered on the permanent record, and are computed into the student's grade point average. We accept the HuskyCT default for letter grades.

**Due Dates and Late Policy**

All course due dates are identified in the Course Schedule in HuskyCT. Deadlines are based on Eastern Time; if you are in a different time zone, please adjust your submission times accordingly. The instructor reserves the right to change dates accordingly as the semester progresses. All changes will be communicated in an appropriate manner.

**I do not accept late assignments.** If you have an emergency, please contact the professor as soon as possible.

**Feedback and Grades**

I will make every effort to provide feedback and grades within 10 days. To keep track of your performance in the course, refer to My Grades in HuskyCT.

Do your own work. I will follow all procedures set in place by The Graduate School for academic integrity. All parties involved will receive a zero for the assignment, will be reported to The Graduate School, and will have final course grades lowered by **at least** one letter grade. Serious misconduct may result in an F for the course along with a recommendation for expulsion from the University.

Be a team player. If I find that you have not contributed to a group project, you will receive a zero for the group project and are also subject to final grade lowering. No excuses.

**Weekly Time Commitment**

You should expect to dedicate **9–12 hours a week to this course**. This expectation is based on the various course activities, assignments, and assessments and the University of Connecticut's policy regarding credit hours. More information related to hours per week per credit can be accessed at the [Online Student website](https://onlinestudent.uconn.edu/learn-more/#collapsepanel-269-1-0-07).

**Student Authentication and Verification**

The University of Connecticut is required to verify the identity of students who participate in online courses and to establish that students who register in an online course are the same students who participate in and complete the course activities and assessments and receive academic credit. Verification and authentication of student identity in this course will include:

- Secure access to the learning management system using your unique UConn NetID and password.
- Routine interactions via email, phone, and video
- Student-created videos and video assignments
- Recorded assessment submissions

## AI Policy

I think we all can identify AI slop when we see it. My promise to you is that I will not serve you AI garbage, and I expect you to return the kindness. We are on the leading edge of technology (!) and are using state-of-the-art tools and methods — and it might be tempting to just copy/paste stuff and think you've mastered it — but it's a big mistake. It's kind of like watching someone doing math — it might make sense while they are doing it, but if you can't do it yourself (without notes), you really don't know it. Use your authentic voice (it's so much better than a generic voice), use GenAI to help you write code but don't copy/paste without understanding what you did. If you code it/write it and you can't defend it, I will be forced to deduct major points (including giving a 0) because it shows you didn't learn anything.

Here was my prompt to an LLM to rewrite my ideas for an AI policy — note how I didn't say 'write me an AI policy for my class.' I hope you see how I use AI and it will inspire your use!

> "ok now let's update my AI use policy. let's craft to be my voice. I believe in students doing their own work, and that AI is a tool, but my course materials are the source. If students are doing ridiculous gymnastics and advanced code/methods that we haven't talked about in class, that means students weren't really present for class. frankly, at this stage in your career, you should turn the AI off and try to learn without it. It's a helpful crutch for getting models to run, but above all, i expect your analysis and business recommendations to be your own voice. on the job, you will have to talk and write WITHOUT AI — which is why I have you talking and writing in class! Practice here and put your honest self forward — don't be afraid! i use AI to help use a more professional voice, but it's almost always a revising tool/interactive tool to make better materials, not a blind blasting of code or text."

Here is the rewrite from the LLM on my AI policy. They both say the same thing — use it as a TOOL not as a "cheat code" to get your homework done. Life is about learning and not copy/pasting.

> "I believe strongly in students doing their own work. AI tools can be helpful, but they are not a substitute for learning, engagement, or original thinking. In this course, the lectures, assignments, and course materials are your primary sources, and your work should reflect the methods, tools, and level of sophistication we have actually covered in class.
>
> Using AI as a lightweight support tool — for example, to help debug code, understand error messages, or revise writing for clarity and professionalism — is acceptable. However, if your submissions rely on advanced techniques, complex code, or modeling approaches that we have not discussed, that is a signal that you were not meaningfully present for the course. At this stage in your career, it is often better to turn AI off, struggle a bit, and learn how things work on your own.
>
> Your analysis, interpretation, and business recommendations must be in your own voice. On the job, you will be expected to explain your decisions, defend your assumptions, and communicate clearly — both verbally and in writing. That is why this course emphasizes discussion, reflection, and presentation. Practice here, be honest about what you know and don't know, and don't be afraid to put your real thinking forward."

I use AI all the time — but as a revision, refinement, or interactive thinking tool, not as a way to blindly generate code or text. I expect you to take the same approach: use AI thoughtfully and transparently, in ways that support learning rather than replace it.

## Student Responsibilities and Resources

As a member of the University of Connecticut student community, you are held to certain standards and academic policies. In addition, there are numerous resources available to help you succeed in your academic work. Review these important [standards, policies and resources](https://onlinestudent.uconn.edu/learn--more/#POL), which include:

- The Student Code
  - Academic Integrity
  - Resources on Avoiding Cheating and Plagiarism
- Copyrighted Materials
- Credit Hours and Workload
- Netiquette and Communication
- Adding or Dropping a Course
- Academic Calendar
- Policy Against Discrimination, Harassment and Inappropriate Romantic Relationships
- Sexual Assault Reporting Policy

## Statement on AI

As your instructor, I want you to know that I occasionally use generative AI to create, enhance, or scale activities in class, as well as to revise or summarize text. It truly is an amazing time we live in, and my role as your professor is to be a guide on your learning journey rather than a strict gatekeeper of information.

My motto this year is "build, build, build (with AI!)". I believe using this technology saves me time that I can devote to providing substantive feedback, creating meaningful course content, and engaging in one-on-one interactions with you. I enthusiastically welcome conversations about how we can use AI meaningfully in the classroom and the workplace, and I'm open to your feedback on my own use of AI in our class.

I promise to deliver you thoughtful, valuable content — not blind-copied, AI-generated filler. I expect you to do the same. Use AI to assist you, not to replace you. This is not a copy/paste class but one where you scale and sharpen your own ideas. As graduate students, I expect you to be creative, quantitative communicators and builders — I expect the best from you!

## Students with Disabilities

The University of Connecticut is committed to protecting the rights of individuals with disabilities and assuring that the learning environment is accessible. If you anticipate or experience physical or academic barriers based on disability or pregnancy, please let me know immediately so that we can discuss options. Students who require accommodations should contact the Center for Students with Disabilities, Wilbur Cross Building Room 204, (860) 486-2020 or <http://csd.uconn.edu/>.

Blackboard measures and evaluates accessibility using two sets of standards: the WCAG 2.0 standards issued by the World Wide Web Consortium (W3C) and Section 508 of the Rehabilitation Act issued in the United States federal government. (Retrieved March 24, 2013 from [Blackboard's website](http://www.blackboard.com/platforms/learn/resources/accessibility.aspx))

For information on managing your privacy at the University of Connecticut, visit the [University's Privacy page](https://privacy.uconn.edu/).

**NOTE:** This course has NOT been designed for use with mobile devices.

## Help

[Technical and Academic Help](https://onlinestudent.uconn.edu/frequently-asked-questions/) provides a guide to technical and academic assistance.

This course is completely facilitated online using the learning management platform, [HuskyCT](http://huskyct.uconn.edu/). If you have difficulty accessing HuskyCT, you have access to the in person/live person support options available during regular business hours through the [Help Center](http://helpcenter.uconn.edu/). You also have [24x7 Course Support](http://www.ecampus24x7.uconn.edu/) including access to live chat, phone, and support documents.

## Library

The MSBAPM program has a liaison at the library who can help you with your research skills. Please refer here <https://guides.lib.uconn.edu/bapm> for information on useful research resources (databases, citation formats, contact information for our dedicated librarian, etc.)

## Minimum Technical Skills

To be successful in this course, you will need the following technical skills:

- Use electronic mail with attachments.
- Save files in commonly used word processing program formats.
- Copy and paste text, graphics or hyperlinks.
- Work within two or more browser windows simultaneously.
- Open and access PDF files.
- Use a second monitor

University students are expected to demonstrate competency in Computer Technology. Explore the [Computer Technology Competencies](http://geoc.uconn.edu/computer-technology-competency/) page for more information.

## Evaluation of the Course

Students will be provided an opportunity to evaluate instruction in this course using the University's standard procedures, which are administered by the [Office of Institutional Research and Effectiveness](http://www.oire.uconn.edu/) (OIRE).

Additional informal formative surveys may also be administered within the course as an optional evaluation tool.
