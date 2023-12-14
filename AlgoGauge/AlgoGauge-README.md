# Algo Gauge - Abstract

**Abstract:**
Algo Gauge is an innovative web application designed to allow users to interactively test and measure the efficiency of various sorting algorithms. It incorporates a real-time queuing system, providing a platform where users can submit algorithm tasks and receive immediate feedback upon completion.

## Introduction
Algo Gauge serves as an educational and practical tool for both students and professionals, aiming to explore algorithmic performance in a controlled environment. This application is user-friendly and is structured to handle concurrent processing efficiently. It consists of a client-server architecture with the client side built using React.js and the server side powered by Node.js and Express.js framework.

## Client-Side Functionality

### Home Page
- **Navigation:** Includes a Navbar.js and Footer.js for sleek navigation.
- **Purpose Introduction:** Guides users towards algorithm selection and testing.

### Testing Page (testing.js)
- **Core Functionality:** Dropdown menu for algorithm selection (SortingAlgorithm.js, SortingAlgorithm2.js, DataStructure.js).
- **Testing Process:** 'Run' button to initiate testing and queue user tasks.

### Queue Modal
- **Real-Time Feedback:** Shows users their position in the queue during high-traffic periods.

### Results Modal (metrics.js)
- **Performance Metrics:** Displays execution time and algorithm efficiency post-task processing.

## Server-Side Functionality

### Queue Management
- **Database Integration:** MongoDB for queue persistence with QueueTable model.
- **Queue Endpoint:** /fullQueue for fetching the current queue state.

### User Position Tracking
- **Endpoints:** /getuserposition and /checkPosition for real-time user position tracking.

### Scheduled Queue Clean-up
- **Efficiency Maintenance:** Periodic cleaning of the oldest queue entry.

## Functionality Across Pages

### Real-Time Updates
- **HTTP Requests:** Utilizes Axios for polling server updates about queued tasks and results.

### Responsive Design
- **UI/UX:** Accessibility across devices, managed by main.scss styles.

### Educational Aspect
- **Learning Platform:** Provides detailed information about each algorithm, enhancing the user experience.

---

Algo Gauge integrates practicality with education, offering a unique platform for understanding and applying efficient algorithms in data processing.
