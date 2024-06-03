<template>
  <div class="app">
    
    <div class="container">
      <aside>
        <nav>
          <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">Dashboard</a></li>
            <li><a href="#">Active Task</a></li>
            <li><a href="#">Active Task</a></li>
            <li><a href="#">Active Task</a></li>
            <li><a href="#">Active Task</a></li>
            <!-- Add more navigation links -->
          </ul>
        </nav>
      </aside>
      <main>
        <div class="task-list">
          <div class="task-item" v-for="task in tasks" :key="task.id">
            <h3>{{ task.title }}</h3>
            <p>Assigned By: {{ task.assignedBy }}</p>
            <p>Assigned To: {{ task.assignedTo }}</p>
            <p>Due Date: {{ task.dueDate }}</p>
            <span :class="{
  'active': task.status === 'Active',
  'OverDue': task.status === 'OverDue'
}">{{ task.status }}</span>

          </div>
        </div>
      </main>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      tasks: [
        {
          id: 1,
          title: 'Explose Task App',
          assignedBy: 'Selva',
          assignedTo: 'SenthilKumar S',
          dueDate: '2024-01-29 13:00:00',
          status: 'Active',
        },
        {
          id: 2,
          title: 'Explose Task App',
          assignedBy: 'Selva',
          assignedTo: 'Dharun S',
          dueDate: '2024-01-22 13:00:00',
          status: 'OverDue',
        },
        {
          id: 2,
          title: 'Explose Task App',
          assignedBy: 'Selva',
          assignedTo: 'Krishnakumar S',
          dueDate: '2024-03-30 13:00:00',
          status: 'Active',
        },
        {
          id: 2,
          title: 'Explose Task App',
          assignedBy: 'Selva',
          assignedTo: 'Pravin B',
          dueDate: '2024-01-05 01:00:00',
          status: 'Active',
        },
        // Add more task objects as needed
      ],
    };
  },
};
</script>

<style>
aside {
  /* Basic styling for the aside element */
  background-color: #f0f0f0;
  padding: 1rem;
  width: 200px; /* Adjust the width as needed */
}

aside nav {
  /* Styling for the nested nav element */
  display: flex;
  flex-direction: column;
}

aside ul {
  /* Styling for the unordered list */
  list-style: none;
  padding: 5%;
  margin: 0;
  padding-left: 10%;
}

aside li {
  /* Styling for each navigation item */
  margin-bottom: 0.5rem;
}

aside a {
  /* Styling for the anchor tags within navigation items */
  text-decoration: none;
  color: #333;
  font-weight: bold;
  transition: color 0.2s ease-in-out;
}

aside a:hover {
  /* Hover effect for navigation links */
  color: #007bff;
}

/* Reset some default styles */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* Basic styles for the app */
.app {
  font-family: Arial, sans-serif;
  line-height: 1.5;
}

/* Container styles */
.container {
  display: flex;
}

/* Sidebar styles */
aside {
  background-color: #f2f2f2;
  padding: 20px;
  width: 200px;
  position: fixed; /* Add this line to make the sidebar fixed */
  top: 9%; /* Add this line to position the sidebar at the top */
  left: 0; /* Add this line to position the sidebar at the left */
  height: 100vh; /* Add this line to make the sidebar span the full height */
}

nav ul {
  list-style-type: none;
}

nav ul li {
  margin-bottom: 10px;
}

nav ul li a {
  text-decoration: none;
  color: #333;
}

/* Main content styles */
main {
  padding: 20px;
  margin-left: 200px; /* Add this line to create space for the sidebar */
  flex: 1;
}

/* Task list styles */
.task-list {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 20px;
}

.task-item {
  background-color: #f2f2f2;
  padding: 20px;
  border-radius: 5px;
}

.task-item h3 {
  margin-bottom: 10px;
}

.task-item p {
  margin-bottom: 5px;
}

.task-item span {
  display: inline-block;
  padding: 5px 10px;
  border-radius: 3px;
  background-color: #ccc;
  color: #333;
}

.task-item span.active {
  background-color: green;
  color: #fff;
}
.task-item span.OverDue {
  background-color: red;
  color: #fff;
}
</style>