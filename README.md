# Website-Apps-script.js
Simple To-Do List Web App built with HTML, CSS, and JavaScript
function addTask() {
    const taskInput = document.getElementById("taskInput");
    const taskList = document.getElementById("taskList");

    const taskText = taskInput.value.trim();
    if(taskText === "") return;

    const li = document.createElement("li");
    li.textContent = taskText;

    // Bisa klik untuk hapus task
    li.onclick = () => {
        li.remove();
    };

    taskList.appendChild(li);
    taskInput.value = "";
}
