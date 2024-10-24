---
sidebar_label: 'Managed Service Co-Pilot'
---

# Managed Service Co-Pilot

**Status:** Not Started

**What:** Managed Service Co-Pilot  
**Why:** Many managed service teams are overwhelmed with the sheer number and variety of support tickets that they see every day. Categorisation of incoming tickets is a great way of helping the team take the first steps to providing the right kind of help to a particular problem. While some teams ask customers to self categorise tickets, many customers don't do this well and the support team has to spend a significant amount of time categorising tickets before they can begin work on a resolution.  
**How:** A chatbot / virtual assistant / LLM could be used to categorise incoming tickets, and potentially take automatic action to provide customers with the support they need, or even take automatic actions to start to resolve the reported issue if enough information is provided.  


### Overview of Challenges Faced by Support Teams
1.	Documentation Sprawl  
Its hard for support teams to find the necessary / relevant documentation quickly and delay the resolution of the ticket – which may result in SLA’s being breached.
Teams often keep documents in large stores like sharepoint or wikis or other dedicated tools. If you have a lot of customers, this can result in a lot of bespoke documentation. Finding the right documentation can often be a hit or miss affair, unless you know where to look, which isn’t always the case with new members of the team.
2.	Information Overload  
Service desk staff are expected to remember too much information.  If you have many customers its hard to know what your SLA’s are – never mind stay within them!
3.	Limited Scalability  
Scaling a service desk team is difficult. The more clients you have, the more people you need. Finding the right people with the right skills is very hard and can be costly.
4.	Maintaining Profitability  
We need to find solutions that allow us to scale our efficiency and allow our staff to do more work, with higher accuracy in shorter timescales. It’s the reason we’re in business. Doing this in a way that is easier and more enjoyable for staff is always better than working them harder.

### Basic Workflow
1.	Summarise support ticket (using categorisation from previous tickets).
2.	Sort and categorise customer data into intents (again, using historical data).
3.	Craft example replies for conversation designers to use as is or as inspiration to brainstorm dialogue.
4.	Transform factual replies to customer requests into a specific tone of voice.
5.  Point support team at appropriate runbooks to resolve the issue.
5.	Implement automations to perform necessary tasks to resolve the ticket.

### Test Implementation
1.	Summarise the tickets with Chat GTP

    Using the following prompt:
    
    Summarize the following customer service interaction. Detect the customer's sentiment and extract any key dates, systems, services or products in the following format.
	Summary:
    Customer Sentiment:

    For example, the following ticket would produce the given response:

    “I cannot setup an Azure Devops repository to store my application code and I have a customer deadline on the 25th December. Please can you setup a repository for me with the name 'Knowledge-Base' and give me administrator access ASAP.”  
    **Summary:** The customer is experiencing difficulty setting up an Azure DevOps repository for storing their application code. They have a pressing customer deadline on the 25th December. The customer is requesting assistance to set up a repository named 'Knowledge-Base' and is seeking administrator access as soon as possible.  
    **Customer Sentiment:** The customer's sentiment appears to be anxious and urgent, driven by the approaching deadline and the need for immediate assistance with the Azure DevOps setup.  
    **Key Dates:** Deadline: 25th December  
    **Key Solutions:**  
        Azure DevOps (platform)  
    **Key Products:**  
        'Knowledge-Base' (name of the requested repository)  
  
### Supporting Links / Investigations  
* https://www.syntera.ch/blog/2023/05/09/ai-driven-ticket-management-implementing-chatgpt-and-python-for-it-support/
* https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/fine-tuning?tabs=turbo%2Cpython&pivots=programming-language-studio
* https://internalnote.com/chatgpt-categorization/
* https://www.linkedin.com/pulse/boosting-support-ticket-analysis-chatgpt-step-by-step-guide/
* https://simplified.com/blog/ai-writing/how-to-train-chatgpt
* https://www.kaggle.com/datasets/suraj520/customer-support-ticket-dataset
* https://earlynode.com/prompt-engineering/chatgpt-prompts-to-answer-support-tickets
* https://www.youtube.com/watch?v=vnUd14bjzho
* https://www.google.com/search?q=using+azure+chatgtp+to+summarise+support+tickets&oq=using+azure+chatgtp+to+summarise+support+tickets&gs_lcrp=EgZjaHJvbWUyBggAEEUYOTIKCAEQABiiBBiJBdIBCTEwMzAzajBqMagCALACAA&sourceid=chrome&ie=UTF-8


