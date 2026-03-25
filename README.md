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
Next I configured the **Booking Management** topic which includes specific instructions for handling guest bookings, ensuring that the topic is aligned with the resort's commitment to seamless guest service. 

### Booking Management Topic Configuration Image
<img width="1919" height="868" alt="Booking Management Topic configuration" src="https://github.com/user-attachments/assets/a2c19775-eb35-4f00-9fa0-0cc3f89e27c9" />
