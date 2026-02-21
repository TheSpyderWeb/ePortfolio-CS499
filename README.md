# Recipe Roulette ePortfolio

This ePortfolio presents my **CS 499 Capstone Project**, showcasing my skills in software engineering, algorithms & data structures, and databases through the **Recipe Roulette** project. This project demonstrates my growth throughout the Computer Science program at SNHU.

---

## Table of Contents
- [Professional Self-Assessment](#professional-self-assessment)  
- [Code Review Video](#code-review-video)  
- [Artifacts](#artifacts)  
  - [Enhancement 1: Software Design and Engineering](#enhancement-1-software-design-and-engineering)  
  - [Enhancement 2: Algorithms and Data Structures](#enhancement-2-algorithms-and-data-structures)  
  - [Enhancement 3: Databases](#enhancement-3-databases)  
- [Demo](#demo)  
- [Project Structure](#project-structure)  
- [License](#license)  

---

## Professional Self-Assessment
Throughout the Computer Science program, I’ve grown from someone who could complete assignments into someone who can design, evaluate, and improve real software systems. Building my ePortfolio and enhancing my Recipe Roulette project forced me to step back and look at my work the way an employer or engineering team would. Instead of asking, “Does this work?” I started asking, “Is this scalable? Is it secure? Is it maintainable? Would another developer understand this?”
One of the biggest areas of growth for me has been understanding how all parts of a system connect. In earlier courses, I focused heavily on writing code that met requirements. Over time, especially through projects like Recipe Roulette, I began thinking more about architecture. I implemented Firebase Authentication for secure user login, structured Firestore around user UIDs to ensure proper data isolation, and applied security rules to protect user data. Moving from LocalStorage to a cloud-hosted database made me think more like a full-stack developer rather than just a front-end programmer.
Collaboration has also been an important part of my growth. In multiple courses, I worked with peers on design discussions, code reviews, and shared problem-solving. I learned how to communicate technical ideas clearly, explain trade-offs, and accept feedback. Through documenting my code and improving readability in Recipe Roulette, I practiced writing software that others can understand and build on. That’s something I now see as essential in professional environments.
My understanding of data structures and algorithms also evolved throughout the program. In my enhancement of the favorites feature, I replaced an array-based lookup (O(n)) with a Map that allows constant-time lookups (O(1)). While the change was small in terms of code, it reflects something bigger: I can analyze time complexity, evaluate performance trade-offs, and apply appropriate data structures in real-world scenarios. This is a skill I developed through courses like Data Structures and Algorithms and strengthened through hands-on implementation.
Software engineering principles became more meaningful as I moved through the program. I learned about the software development lifecycle, iterative testing, modular design, and separation of concerns. In Recipe Roulette, I organized functionality into modules for authentication, meal handling, and navigation. I improved documentation, standardized UI behavior, implemented consistent error handling, and tested features repeatedly to ensure reliability. These decisions reflect industry practices rather than just academic requirements.
Database design was another major area of growth. Through SQL coursework and hands-on Firebase implementation, I learned how to structure data intentionally instead of storing it casually. Organizing user favorites under authenticated UIDs strengthened my understanding of access control, scalability, and persistence. It also reinforced how backend architecture directly affects user experience.
Security awareness is something I now actively consider in development. By implementing Firebase Authentication, Firestore security rules, and input validation, I had to think about how users interact with data and how to prevent unauthorized access. I also practiced handling authentication state changes and providing meaningful error feedback to users. This mindset of anticipating potential misuse or vulnerabilities is something I will carry into future development roles.
All of these experiences have shaped my professional goals. I aim to work in software engineering, specifically full-stack development, where I can design and build systems that solve real problems. My artifacts in this portfolio, particularly Recipe Roulette and its enhancements, demonstrate growth across software design, algorithms, databases, and security. Together, they show that I can evaluate existing systems, implement meaningful improvements, and communicate technical decisions clearly.
This ePortfolio represents more than completed assignments. It reflects my transition into a developer who thinks about structure, efficiency, collaboration, and security — not just functionality. I am confident that the skills demonstrated here prepare me to contribute effectively in a professional software engineering environment.
  

*Reflection:* Completing the Recipe Roulette project allowed me to integrate my knowledge from multiple courses while demonstrating my problem-solving and full-stack development skills. The enhancements showcase my ability to produce professional-quality software aligned with industry standards.

---

## Code Review Video
Video link:https://youtu.be/sUcE-wRmXvI

---

## Artifacts

### Enhancement 1: Software Design and Engineering
For this milestone, I chose my Recipe Roulette web app as the artifact for my ePortfolio. I originally built this project in a previous course as a full-stack web application that helps users discover recipes, search by ingredients or name, save favorites, and manage their accounts. It integrates TheMealDB API for recipe data, Firebase Authentication for login and sign-up, and Firestore for storing user-specific data.
I selected this project because it brings together front-end development, back-end integration, API communication, and database design in one cohesive system. It’s not just a static website, it’s a functioning application with authentication flow, user state management, and persistent data.
For the first enhancement, I focused on improving maintainability, usability, and overall structure. First, I added detailed comments across all JavaScript files. Instead of leaving logic unexplained, I documented what each function does, how Firebase interactions work, and how user state is handled. This makes the code easier to understand for collaborators or future developers and reflects real-world code review standards.
Second, I improved the layout and usability of the favorites section. Previously, the favorites container would cut off after five recipes, which created a poor user experience. I redesigned the CSS layout and made the container scrollable so it can handle any number of saved recipes without breaking the UI. This was a small visual change, but it required careful testing to make sure it didn’t affect responsiveness or other elements on the page.
Third, I standardized the navbar and button behavior across all pages. Login, sign-up, and logout buttons now behave consistently depending on authentication state. I also ensured proper redirects after login and logout and added clear error messages in the UI when authentication fails. This improved both usability and reliability.
Through this enhancement, I demonstrated my ability to evaluate an existing system, identify weak points, and refine it using software engineering principles. I practiced iterative testing, improved code documentation, and made design trade-offs that balanced usability with maintainability. This aligns strongly with course outcomes related to designing computing solutions, communicating technical decisions clearly, and implementing professional-quality software.
More than anything, this milestone reflects growth. I didn’t just build something that works, I improved it to be cleaner, more maintainable, and more user-centered.


### Enhancement 2: Algorithms and Data Structures
For the algorithms and data structures enhancement, I focused on optimizing the favorites feature in Recipe Roulette.
Originally, I stored favorite meal IDs in an array. Every time I needed to check whether a meal was already saved, I had to loop through the entire array. That meant each lookup was O(n) time complexity. While this worked for small amounts of data, it doesn’t scale well as the number of favorites grows.
To improve efficiency, I replaced the array-based lookup approach with a JavaScript Map. Each meal ID is now stored as a key, and the full meal object is cached as the value. This allows instant lookups in O(1) time complexity.
-
The Map is used strictly for in-memory performance, while Firestore remains the source of truth for persistent storage. This means:
•	Firestore stores user favorites long-term.
•	The Map improves runtime efficiency during a session.
•	I reduce unnecessary API calls because cached meals don’t need to be re-fetched.
I tested this enhancement by repeatedly adding and removing favorites, refreshing the page, and monitoring performance behavior in the console. The app feels noticeably more responsive.
-
This change may seem small, but it demonstrates something important like choosing the correct data structure matters. It shows that I can analyze time complexity, identify inefficiencies, and apply algorithmic principles to improve real-world software performance. That directly aligns with the course outcome related to designing and evaluating computing solutions using algorithmic principles and managing trade-offs.
Instead of just writing code that works, I made it more efficient and scalable.


### Enhancement 3: Databases
For the database enhancement, I focused on transitioning Recipe Roulette from local storage to a more scalable and secure database architecture using Firebase Firestore.
Originally, favorite recipes were stored in the browser using LocalStorage. While that approach worked for simple persistence, it had major limitations:
•	Data was tied to a single device.
•	Users couldn’t access favorites across sessions or devices.
•	There was no structured user isolation.
To address this, I migrated the favorites feature to Firestore and structured the database around authenticated users. Each user’s favorites are now stored under their unique Firebase Authentication UID. This ensures that user data is logically separated and associated only with the correct account.
Firestore now acts as the persistent data layer, while the front end retrieves and updates data securely through Firebase SDK calls.
#
In addition to restructuring storage, I implemented:
•	Firebase Authentication for secure user identity management
•	Firestore security rules to ensure users can only access their own data
•	Input validation before writing to the database
•	Clear UI error handling for failed operations
#
This enhancement demonstrates a stronger full-stack architecture. Instead of relying on client-side storage, I implemented a cloud-hosted NoSQL database solution with proper authentication and security boundaries.
$
This aligns directly with the course outcome focused on developing a security mindset. I had to think about:
•	Data isolation between users
•	Preventing unauthorized reads/writes
•	Validating inputs before storing data
•	Handling authentication states securely
#
By moving from LocalStorage to Firestore with UID-based organization and security rules, I transformed the app from a basic client-side project into a more production-ready full-stack application.


---

## Demo
Video link:https://youtu.be/spKugOYgpIc

---
## 👩‍💻 Author

Reeham Imam  
Computer Science Student  
Southern New Hampshire University  
