# Agentforce AI Concierge for Coral Cloud Resorts.

## Use Case & Business Requirements:

Coral Cloud Resorts, a luxury seaside destination, is well-known for its seasonal offerings and dedication to providing personalized, high-quality guest experiences. Typically, the resort has its busiest season in the summer, with quieter off-season months. However, this year, the resort faces an exciting but complex challenge: An independent film festival is being hosted nearby during the off-season. This event is expected to draw a large volume of new and returning guests.

Adding to the excitement, Coral Cloud Resorts is to host several exclusive festival meet-and-greet events onsite. These high-profile activities, combined with increased guest demand, create unique operational pressures for the resort.

To meet these demands, Coral Cloud Resorts is expanding service hours, offering exclusive film festival-related activities, and rolling out new event options—all while maintaining high standards of guest service. To achieve this without significantly increasing staffing, the resort is turning to automation and artificial intelligence (AI)-driven customer service solutions.

### Business Requirements:
- Set up and configure the Coral Cloud Experience Agent to deliver personalized, accurate responses using trusted data sources like the Agentforce Data Library and Knowledge articles.
- Equip the agent with actions to modify guest bookings, such as adding or canceling reservations, and provide real-time booking information.
- Use topics like General FAQs to handle common questions and create custom topics to highlight festival-related offerings.
- Set up routing flows to transfer unresolved or complex guest queries to service representatives for further assistance.

### ROI
- The Coral Cloud Experience Agent aims to help the resort maintain exceptional guest service during the busy festival season while optimizing staff workloads.

## Solution:
### Step 1: Defining Role & Context

<img width="1917" height="869" alt="Define Agent Role and Context " src="https://github.com/user-attachments/assets/2f651f8e-1224-495a-921b-9d2428d66489" />

### Step 2: Integration of knowledge articles within the Agenforce Builder
I started by managing the data sources to provide access to the knowledge articles. I did this by creating 2 data libraries, one for the knowledge articles called **Coral Cloud Experience Agent Library** and another for the code of conduct agreement pdf file called **Code of Conduct Agreement**. 

### Coral Cloud Experience Agent Library Configuration
**Image 1**
<img width="1919" height="866" alt="Configure Data Library - 1" src="https://github.com/user-attachments/assets/3cc35368-659c-41d1-b24d-9cd3f9c57d81" />
**Image 2**
<img width="1917" height="867" alt="Configure Data Library - 2" src="https://github.com/user-attachments/assets/4ae5c226-85d8-4eac-a425-b80114982099" />

### Step 3: Booking Management Topic & Agent Actions
Next I configured the **Booking Management** topic which includes specific instructions for handling guest bookings, ensuring that the topic is aligned with the resort's commitment to seamless guest service. The Booking Management topic has 3 actions associated with it, the **Get Booking**, **Adjust Booking** and **Cancel Booking**, which aim to support with booking information retrieval, booking modifications and booking cancellations respectively.

### Booking Management Topic Configuration
<img width="1919" height="868" alt="Booking Management Topic configuration" src="https://github.com/user-attachments/assets/a2c19775-eb35-4f00-9fa0-0cc3f89e27c9" />

### Get Booking Agent Action Configuration
<img width="1919" height="871" alt="Get Booking Agent Action" src="https://github.com/user-attachments/assets/1683ca21-e834-44fa-9ae1-b42cf2c8dc62" />

### Adjust Booking Agent Action Configuration
<img width="1919" height="874" alt="Adjust Booking Agent Action" src="https://github.com/user-attachments/assets/90b98820-23d6-4e14-a7ec-3ee6943ab495" />

### Cancel Booking Agent Action Configuration
<img width="1919" height="877" alt="Cancel Booking Agent Action" src="https://github.com/user-attachments/assets/b96a79b9-5489-4934-b73c-863da451d4c9" />

### Step 4: Add Standard Topics & General FAQ & Escalation
In this step I aim to ensure the agent uses trusted data sources, such as Knowledge articles and the Code of Conduct PDF, for accurate responses. Additionally, I ensure the agent can escalate complex queries to a service representative when necessary.
To do this I had to use an agent action to invoke the Film_Festival_Related_Answers prompt template. The prompt template generates a response to the user’s question based on the relevant information from Knowledge articles and the Code of Conduct file. I then had to set the guardrails to get answers from the response of the Film_Festival_Related_Answers prompt template, then create a new action to invoke the prompt template and then associate this new action to the General FAQ topic.

### Film_Festival_Related_Answers Prompt Template
<img width="1919" height="868" alt="Prompt Template Configuration" src="https://github.com/user-attachments/assets/f67e933f-3e45-4dd6-92e9-5135d2a53ca9" />

### Testing the Prompt Template
<img width="1919" height="872" alt="Testing the Prompt Template" src="https://github.com/user-attachments/assets/73404a8d-dfcc-4298-a631-e42380dd63b2" />

### Agent Action to invoke Prompt Template
<img width="1919" height="874" alt="General FAQ Agent Action (prompt template)" src="https://github.com/user-attachments/assets/cec88ea6-2f84-4e27-bfa4-64843d703ee1" />

### Step 5: Deploy Agent
In this step I deploy the agent to the Coral Cloud Resort's Experience Cloud site. To do this successfully I first configured the inbound omnichannel flow, Route to ESA, to transfer conversations from guests on the site to the Coral Cloud Experience Agent. In situations where the guests require assistance from a service representative, the org is equipped with the outbound omnichannel flow, ESA - Route to Queue. The Coral Cloud Experience Agent uses this flow to route escalations to a Messaging queue. I then published the ESA Web Deployment Embedded Service, added the Embedded Messaging component to the coral cloud site, and published the site. 

### Testing the Agent
<img width="1919" height="871" alt="Testing Agent" src="https://github.com/user-attachments/assets/674aaa1d-527b-46f2-a1c4-c2752eeae23d" />

### Route to ESA Flow Configuration
<img width="1919" height="873" alt="Route to ESA configuration" src="https://github.com/user-attachments/assets/dbbf4813-b7d0-4c74-b40e-37cc98769b12" />

### Publishing ESA Web Deployment Embedded Service 
<img width="1918" height="871" alt="Publishing Embedded Service" src="https://github.com/user-attachments/assets/33c265a9-4353-4bd6-aeae-1c43fc58abbd" />

### Adding Embedded messaging component to Experience Cloud Site
<img width="1919" height="870" alt="Embedded Messaging on Experience Cloud" src="https://github.com/user-attachments/assets/2d428d67-aca7-42d9-9431-6aca2c458eb8" />

### Publishing Experience Cloud Site
<img width="1919" height="870" alt="Publishing Experience Cloud Site" src="https://github.com/user-attachments/assets/b22a8fbd-de5e-4f0a-98c7-d734f33ed85d" />

