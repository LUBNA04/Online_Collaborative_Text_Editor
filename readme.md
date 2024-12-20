Online Collaborative Text Editor
Table of Contents
Introduction
Features
Tech Stack
How to Run

Introduction
This project is a fully functional online real-time collaborative text editor designed for individuals and teams to create, edit, and share documents efficiently. Unlike traditional editors, this tool allows simultaneous collaboration, ensuring a seamless experience with real-time updates and version control.

Its intuitive user interface and robust backend ensure high performance, scalability, and security.

Features
User Management
Secure Login & Registration: User authentication with encrypted credentials.
Session Management: Maintain secure sessions with automatic timeout.
Document Management
Create, Share, and Manage Files:
Users can create, rename, delete, and manage access to files.
Control access by assigning permissions (viewer/editor).
Activity Log: Track changes and edits made by collaborators.
Real-Time Collaboration
Simultaneous Editing: Multiple users can edit documents in real-time with minimal latency.
Conflict Resolution: Built-in mechanisms to handle simultaneous edits using CRDT (Conflict-Free Replicated Data Type).
Live Cursors: View other collaborators' cursor positions and edits.
Enhanced Editing Experience
Rich Text Formatting: Add bold, italic, and other formatting styles.
Commenting: Inline comments for effective communication during collaboration.
Version Control: Undo and redo options with edit history tracking.
UI/UX
User-Friendly Interface: Streamlined design for document management and editing.
Mobile Responsive: Optimized for desktop and mobile use.
Tech Stack
Backend
Java
Spring Boot (REST API)
WebSocket (STOMP Protocol for real-time updates)
Spring Security (JWT for authentication)
MySQL (Database)
Frontend
React.js
Quill.js (Rich text editor)
Socket.io (for real-time updates)
How to Run
1. Clone the Repository
sh
Copy code
git clone https://github.com/yourusername/Online-Collaborative-Text-Editor.git
2. Backend Setup
Navigate to the backend directory:

sh
Copy code
cd Online-Collaborative-Text-Editor/backend
Build the project:
sh
Copy code
./gradlew build
Run the Spring Boot server:
sh
Copy code
./gradlew bootRun
3. Frontend Setup
Navigate to the frontend directory:

sh
Copy code
cd ../frontend
Install dependencies:
sh
Copy code
npm install
Start the development server:
sh
Copy code
npm start
4. Access the Application
Open your browser and go to http://localhost:3000 to access the application.

Screenshots
Login Page
(Add a screenshot with your branding)

Collaborative Editing
(Replace with a unique screenshot of collaborative editing in action)

Demo
(Upload your own demo video and replace this link)
Demo Video

Algorithm
The editor uses a Conflict-Free Replicated Data Type (CRDT) model to resolve conflicts during simultaneous edits.

Key Highlights:
Node Representation: Each character in the document is represented as a node containing:
Node ID
Metadata (bold, italic)
Left and right pointers (as in a doubly linked list)
Conflict Resolution: Conflicts are resolved by assigning priorities based on user operations and usernames.