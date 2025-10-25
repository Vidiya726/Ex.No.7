# Exno.7-Develop a prompt-based application tailored to their personal needs, fostering creativity and practical problem-solving skills while leveraging the capabilities of large language models.

# Date:
# Register no.
# Aim: To develop a prompt-based application using ChatGPT - To demonstrate how to create a prompt-based application to organize daily tasks, showing the progression from simple to more advanced prompt designs and their corresponding outputs.

#AI Tools Required: 


# Explanation: 
Prompt:
"Design a personal productivity assistant that can help manage daily tasks, schedule reminders, suggest wellness tips, and answer general queries. The assistant should interact using natural language and be adaptable to the user’s changing preferences over time."
Procedure:
1. Define the core requirements of a personal productivity assistant.
2. Identify and construct appropriate prompts for each task using an LLM (e.g., ChatGPT).
3. Simulate natural user interaction through a simple interface or command-line system.
4. Collect feedback or inputs from users and adapt responses accordingly.
5. (Optional) Integrate basic memory to simulate preference adaptation.
EXPECTED OUTPUT: - (attached the drive link)
Output (Example Response by LLM):
Personal Productivity Assistant Features:
1. Daily Task Manager:
o Accept tasks via natural language (e.g., "Remind me to call mom at 6 PM").
o Organize tasks by priority and deadline.
o Provide daily summaries and pending items.
2. Smart Scheduler:
o Schedule events and set reminders using contextual understanding.
o Notify user of overlapping appointments or free time slots.
3. Wellness Tips Generator:
o Suggest daily wellness advice (hydration, exercise, screen-time breaks).
o Adapt suggestions based on past user preferences and responses.

# Output:
## Personal Productivity Assistant Application Design: Full Structure

## 1. Core Requirements and Conceptual Design (Foundation)

This phase establishes the foundational blueprint for the assistant, defining its purpose, user interaction style, and essential technical capabilities.

### 1.1 Defining the Assistant's Persona and Interaction

The assistant must function as a trusted digital partner, not just a rigid tool.

* **Target User Profile:** The application is optimized for individuals managing multiple responsibilities (e.g., professionals, students) who need structure but prefer **flexible, natural language interaction** over formal commands.
* **Tone and Style (Natural Language):** The interaction must be conversational and supportive. The LLM's output must adopt a tone that is **Helpful, Encouraging, and Concise**. Responses should be direct, yet friendly, avoiding technical jargon. This ensures user trust and continuous engagement.
* **Interaction Modality:** The primary mode is **Text-based Input/Output** (simulated command line or chat interface). The system must robustly handle complex, informal, or ambiguous inputs (e.g., "Schedule a quick call with Sarah sometime tomorrow morning").
* **Adaptability and Customization:** The assistant must **store and recall** user preferences (e.g., timezone, preferred task viewing format, diet restrictions for wellness tips). This **memory function** is critical for personalizing the experience and fulfilling the prompt's requirement for adaptation.

### 1.2 Required Technical Capabilities (Leveraging the LLM)

These are the necessary functions that allow the application to process information and generate practical results.

* **Natural Language Understanding (NLU):** The system's most crucial capability. It must parse free-form text to accurately identify:
    * **Intent** (e.g., *Schedule*, *Remind*, *Query*, *Prioritize*).
    * **Entities** (e.g., *Date*, *Time*, *Task Description*, *Priority Level*).
* **State Management & Contextual Memory:** The ability to recall *prior* interactions within a single session (short-term memory) and recall *stored* user preferences (long-term memory). This enables the LLM to follow up on previous statements (e.g., User: "Add a task." Next turn: "Make that task high priority.").
* **Output Generation & Formatting:** The LLM generates coherent, grammatically correct, and appropriately formatted responses. The output must be relevant to the intent and align with the user’s stored preference for formality.
* **Integration Points (Simulated):** The structures the LLM interacts with to perform actions: a **Task List** (JSON array or database schema), a **Calendar** (for scheduling checks), and a **Preference File** (for memory storage).
* <img width="672" height="668" alt="image" src="https://github.com/user-attachments/assets/97a672cf-026f-4ad8-bcbd-2d2c065a6555" />



## 2. Feature-Specific Prompt Engineering (LLM Strategy)

This section details how to structure the LLM prompts to handle the core features defined by the task.

### 2.1 Daily Task Manager Prompts
* **Task Input Prompt:** Designed to instruct the LLM to extract the task, deadline, and priority from natural language input and format it into a structured data object.
* **Daily Summary Prompt:** Asks the LLM to review a list of tasks and present them to the user in an organized, motivating format, often prioritizing the top 3 critical items.

### 2.2 Smart Scheduler Prompts
* **Scheduling Prompt:** Instructions to the LLM to parse time and event details from text, and then check against a simulated calendar structure for conflicts.
* **Reminder Creation Prompt:** A focused prompt for translating a time-bound request into a specific, actionable notification message.

### 2.3 Wellness Tips Generator Prompts
* **Context-Aware Suggestion Prompt:** A prompt that integrates stored user preferences (e.g., "User prefers low-impact exercise," or "User needs a reminder to hydrate") to generate a personalized and relevant tip.
* **General Query Prompt:** A flexible, fallback prompt designed to handle any general knowledge question outside the core productivity scope.
<img width="673" height="663" alt="image" src="https://github.com/user-attachments/assets/47ac92b4-1b93-4040-ba81-b4ee6e76aba3" />


## 3. Implementation and User Interaction Flow

This section covers the practical steps for building, refining, and maintaining the assistant.

### 3.1 Simulation Interface Design
* **Input/Output Loop:** The fundamental process of receiving user text, feeding it to the LLM, and displaying the structured response.
* **Command Structure (Simulated):** Defining simple text-based overrides (e.g., typing `!tasks` for a list, or `!settings` to quickly update preferences) for efficiency.

### 3.2 Feedback and Adaptation Mechanism
* **Feedback Collection:** A simple process to gauge user satisfaction (e.g., "Was that tip useful? Yes/No?") to refine future LLM generations.
* **Preference Storage (Simulated Memory):** Using a persistent data structure (e.g., JSON file) to hold and manage user settings like `\{ 'WakeUpTime': '7:00 AM', 'PreferredExercise': 'Yoga', 'ReminderFrequency': 'Daily' \}`.

### 3.3 Testing and Evaluation
* **Scenario Testing:** Running the application through common and complex user cases (e.g., ambiguous scheduling, conflicting appointment requests, and complex priority setting).
* **LLM Response Quality Check:** Continuous evaluation of the LLM's output for coherence, relevance, and adherence to the user's preferred persona and tone.

# Personal Productivity Assistant Application Design: Complete Structure

## 1. Core Requirements and Conceptual Design (Foundation)

This initial phase defines the fundamental blueprint for the assistant, ensuring its functionality aligns with the user's needs for a natural, adaptable, and helpful tool.

### Defining the Assistant's Persona and Interaction

The assistant must be structured as a trusted digital partner capable of natural dialogue. The **Target User Profile** is optimized for individuals managing complex workloads (professionals, students) who require flexible interaction rather than rigid commands. The **Tone and Style** must be conversational, adopting an **Helpful, Encouraging, and Concise** persona to foster user trust and continuous engagement. The primary **Interaction Modality** will be text-based, requiring robust **Natural Language Understanding (NLU)** to process fragmented, informal, or complex sentences, ensuring a high success rate in interpreting user intent. Crucially, the system must be **Adaptable and Customized**, utilizing a **memory function** to store and recall user preferences (e.g., preferred exercise time, work hours, tone preference) to personalize the experience over time.

### Required Technical Capabilities (Leveraging the LLM)

These capabilities map the LLM’s role to the application’s functional requirements. The most important function is **Natural Language Understanding (NLU)**, where the LLM parses free-form text to accurately identify the user's **Intent** (e.g., *Schedule*, *Remind*) and **Entities** (e.g., *Date*, *Time*, *Task Description*). This NLU output is then used by the **State Management & Contextual Memory** system, which allows the assistant to recall **short-term context** within a session and retrieve **long-term preferences** from a connected data store (like a JSON file). Finally, **Output Generation & Formatting** involves the LLM crafting the final response, ensuring it is coherent, grammatically correct, and matches the user's preferred tone and summary style. These actions are performed by interacting with simulated **Integration Points**—structured data tools like a Task List, Calendar, and Preference File—to ensure practical, data-driven results.


## 2. Feature-Specific Prompt Engineering (LLM Strategy)

This critical phase involves crafting precise **"meta-prompts"** that constrain the general-purpose LLM to reliably perform the specific tasks required by the application.

### 2.1 Daily Task Manager Prompts 📋

The task manager's success hinges on converting unstructured user requests into actionable, structured data.

* **Task Input & Parsing:** The LLM receives an explicit instruction: "You are a Task Parser. Analyze the following user text. Extract the **task description**, a **due date/time** (in YYYY-MM-DD HH:MM format, inferring if necessary), and the **priority level** (High, Medium, Low). If any element is missing, use 'None' or 'Medium'." The expected output is a structured JSON object, making it easy to store in the Task List.
* **Daily Summary Generation:** The prompt instructs the LLM to review the pending task list and current date, generating a **motivating, concise daily summary** of the top three most urgent items. It must be presented in a friendly, conversational tone, incorporating the user's preference for motivation or formality.
* **Task Editing/Prioritization:** When a user attempts to change a task (e.g., "Make that task high priority"), the prompt directs the LLM to identify the **specific field** that needs modification (e.g., *priority*, *deadline*) and the new value, formatting it for an update query.

### 2.2 Smart Scheduler Prompts 📅

These prompts manage time and resource allocation, often requiring simulated conflict checking.

* **Scheduling & Time Parsing:** The LLM is instructed: "You are an Event Scheduler. Extract the **event title**, **start time**, and **duration** from the user's request. Format the times accurately into a standard datetime object." It is then fed the simulated calendar data and told to check for overlaps. The output is either a successful scheduling object or a flag indicating a conflict.
* **Reminder Creation:** This prompt is focused on translation, instructing the LLM to convert a time-bound request into the final text for an actionable reminder notification, utilizing the user's saved tone (e.g., casual vs. formal).
* **Conflict Resolution:** When a conflict is detected, the prompt requires the LLM to offer **two specific alternative time slots** close to the original request, presenting a clear choice to the user rather than simply denying the request.

### 2.3 Wellness Tips and General Query Prompts 🌱

This uses the LLM's broad knowledge base while ensuring relevance and personalization.

* **Context-Aware Wellness Tip:** The most advanced prompt. It instructs the LLM to "Generate a unique daily wellness tip. **Crucially, integrate the user's stored preferences** (e.g., 'User is vegetarian', 'User likes morning walks'). The tone must be encouraging. Do not repeat the last 5 tips given." This leverages the long-term memory for highly personalized advice.
* **General Query Handling:** This serves as the system's fallback. The prompt instructs the LLM to "Act as a general knowledge expert. Answer the user's query directly and concisely. If the query falls outside your productivity scope, treat it as a factual question."
* **Preference Adaptation/Setting:** When a user explicitly updates their preferences (e.g., "I want my tips to be more formal"), the LLM identifies the **preference field** (e.g., 'TipStyle', 'SleepGoal') and the **new value**, formatting this data for storage in the Preference File.


## 3. Implementation and User Interaction Flow

This section covers the practical steps for developing and refining the application interface and underlying data management.

### 3.1 Simulation Interface Design
The **Input/Output Loop** forms the backbone: user text is input, processed by the LLM via the specialized prompts, and the structured response is displayed. A simple **Command Structure** using non-natural language flags (e.g., `!tasks`, `!settings`) will be implemented to allow for efficient access to common functions, overriding the NLU when speed is preferred.

### 3.2 Feedback and Adaptation Mechanism
**Feedback Collection** will be simulated by occasionally prompting the user for a simple binary response (e.g., "Was that reminder timing helpful? Yes/No?"). The **Preference Storage (Simulated Memory)** will be managed through a persistent JSON or dictionary object, where fields like `\{ 'WakeUpTime': '7:00 AM', 'PreferredExercise': 'Yoga', 'TipStyle': 'Informal' \}` are updated based on user input, ensuring the LLM's future responses are personalized.

### 3.3 Testing and Evaluation
The process concludes with **Scenario Testing**—running the application through complex user cases like ambiguous task inputs or conflicting scheduling requests. A final **LLM Response Quality Check** is conducted to evaluate the coherence, relevance, and overall helpfulness of the generated outputs against the initial design requirements.




# Result: 
The lab exercise resulted in the creation of a prototype concept for a personal assistant powered by large language models. Students were able to:
 Understand how to tailor LLM prompts to real-life applications.
 Foster creativity by designing features suited to their personal or academic lives.
 Learn prompt engineering techniques for optimal interaction with AI tools.
 Experience the versatility and utility of generative AI in solving everyday problems.
