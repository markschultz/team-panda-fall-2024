# team-panda-fall-2024

Architectural Kata Fall 2024

[View as GitHub Pages for HTML rendering](https://markschultz.github.io/team-panda-fall-2024/)

Team:
  - Mark Schultz
  - Cameron Barton ([LinkedIn](https://www.linkedin.com/in/cameronbarton/))
  - Dan Bongard
  - Calvin Poon ([LinkedIn](https://www.linkedin.com/in/calvinpoon/))

## Problem Background
### Problem Statement
The technology industry faces a persistent challenge in achieving a truly diverse and inclusive workforce. Biases, both conscious and unconscious, often seep into the hiring and interview processes, hindering the selection of candidates based solely on merit and skills. Traditional Applicant Tracking Systems (ATS) also contribute to the problem by relying on keyword matching and potentially overlooking qualified candidates from underrepresented groups. This lack of effective tools to identify and mitigate bias perpetuates the under-representation of certain demographics in the tech sector.

### Business Requirements
To address these challenges, the Diversity Cyber Council is developing "ClearView", an AI-powered HR platform designed to promote equitable hiring practices. The platform's key requirements include:
- Anonymized Candidate Profiles: Removing personally identifiable information from resumes to minimize bias during the initial screening.
- AI-Powered Resume Analysis: Leveraging AI to reconstruct resumes into a SMART goal format, highlighting skills and experience relevant to open positions.
- Quantifiable Matching: Implementing a similarity score or matching algorithm to align candidate qualifications with job descriptions objectively.
- AI-Generated Resume Tips: Providing candidates with AI-driven suggestions to improve their resumes and increase their chances of success.
- Bias Mitigation: Ensuring the AI algorithms eliminate potential indicators of race, lifestyle, culture, or other personal attributes that could lead to biased decisions.
- Data Aggregation and Analytics: Collecting and analyzing data on candidate demographics, hiring decisions, and interviewer feedback to identify and address disparities in the hiring process.
- Integration with HR Systems: Enabling seamless integration with popular HR systems to streamline data exchange and workflow.

### Assumptions
- Employers are genuinely committed to fostering diversity and inclusion in their workforce.
- Job seekers are actively looking for a fair and transparent hiring process that values their skills and experience.
- AI technology can be effectively trained and utilized to minimize bias in resume screening and matching.
- Data collection and analysis will provide valuable insights into the effectiveness of diversity and inclusion initiatives.

### Actors and Actions
- Employers: Register on the platform, provide company information, post job descriptions, review anonymized candidate profiles, unlock full profiles, conduct interviews, make hiring decisions, and complete surveys.
- Job Candidates: Register on the platform, upload resumes, receive AI-generated resume tips, view potential matches, contact employers, update or remove resumes, and complete surveys.
- Administrators: Manage the platform, register users, generate data analytics reports, provide solution-building services, and oversee system maintenance.

## C4 Diagrams
- [Container Diagram](c4/C4%20-%20Container%20Diagram.jpeg)
  - [Legend](c4/C4%20-%20Container%20Diagram%20-%20Legend.jpeg)
- [System Context Diagram](c4/C4%20-%20System%20Context%20Diagram.jpeg)
  - [Legend](c4/C4%20-%20System%20Context%20Diagram%20-%20Legend.jpeg)

## Models
This catalog provides a collection of models developed during the design phase of the ClearView system as part of the 2024 Architecture Kata. Each model represents a specific domain or architectural aspect of the system. To explore the detailed models, click on the respective archetype frame below.

- [Models Documentation Main Cover](Models/index.html)
  - [Use Cases](Models/EARoot/EA1/EA1/EA12.html)
  - [Components](Models/EARoot/EA1/EA2/EA74.html)
  - [Activities](Models/EARoot/EA1/EA3/EA129.html)
