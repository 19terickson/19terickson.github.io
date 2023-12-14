Abstract:
Algo Gauge is an innovative web application designed to allow users to interactively test and measure the efficiency of various sorting algorithms. It incorporates a real-time queuing system, providing a platform where users can submit algorithm tasks and receive immediate feedback upon completion.


The increasing complexity of data processing necessitates the understanding and application of efficient algorithms. Algo Gauge steps in as an educational and practical tool for both students and professionals to explore algorithmic performance in a controlled environment. With a user-friendly interface and a backend structured to handle concurrent processing, the platform ensures a seamless experience.
Algo Gauge consists of a client-server architecture where the client side is built using React.js, facilitating dynamic content rendering, and the server side is powered by Node.js with Express.js framework, managing API requests and database interactions.

Client-Side Functionality:

Home Page:
The landing page serves as the entry point to the platform, displaying a sleek navigation bar (Navbar.js) and a footer (Footer.js). It introduces users to the platform's purpose and guides them towards algorithm selection and testing.

Testing Page (testing.js):
This is where users interact with the core functionality of the platform. The page offers a dropdown menu to select different algorithms (managed by SortingAlgorithm.js, SortingAlgorithm2.js, and DataStructure.js) and initiate testing. A 'Run' button triggers the testing process, queuing the user's task for execution.

Queue Modal:
Upon initiating a test run, users are shown their position in the queue. This real-time feedback is crucial, especially during high-traffic periods, to manage expectations. The queuing system is robust, automatically updating and cleaning up entries to maintain efficiency.

Results Modal (metrics.js):
After a task is processed, users are directed to view their test results in a modal window. It displays performance metrics such as execution time and algorithm efficiency, offering valuable insights into algorithm behavior under various conditions.

Server-Side Functionality:

Queue Management:
At the heart of the server-side application is the queuing logic, which utilizes MongoDB for persistence. The QueueTable model keeps track of each user's task, adding and removing entries as they are processed. An endpoint /fullQueue is dedicated to fetching the current state of the queue.

User Position Tracking:
The /getuserposition and /checkPosition endpoints enable real-time tracking of a user's position within the queue. This information is critical for maintaining transparency and setting accurate user expectations.

Scheduled Queue Clean-up:
To ensure the queue remains efficient, a scheduled task periodically cleans up the oldest entry, keeping the system lean and responsive.

Functionality Across Pages:

Real-Time Updates:
Using Axios for HTTP requests, the client-side application regularly polls the server for updates, ensuring that users receive the most current information regarding their queued tasks and results.

Responsive Design:
The UI/UX design, managed by styles defined in main.scss, ensures that Algo Gauge is accessible and functional across various devices and screen sizes.

Educational Aspect:
Each algorithm selection provides an option for users to learn more about it. This educational feature enriches the user experience, making Algo Gauge a learning platform as well as a testing tool.