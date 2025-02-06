<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio SIG</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>Portfolio de Gestion de Rapports SIG</h1>
    </header>
    <main>
        <section id="create-report">
            <h2>Créer un Nouveau Rapport</h2>
            <form id="report-form">
                <label for="title">Titre:</label>
                <input type="text" id="title" name="title" required>
                <label for="description">Description:</label>
                <textarea id="description" name="description" required></textarea>
                <button type="submit">Créer</button>
            </form>
        </section>
        <section id="reports">
            <h2>Liste des Rapports</h2>
            <ul id="report-list"></ul>
        </section>
    </main>
    <script src="script.js"></script>
</body>
</html>body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
}

header {
    background-color: #4CAF50;
    color: white;
    padding: 1em 0;
    text-align: center;
}

main {
    margin: 2em auto;
    padding: 1em;
    width: 80%;
    max-width: 800px;
    background-color: white;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

h1, h2 {
    margin: 0 0 1em 0;
}

form {
    display: flex;
    flex-direction: column;
}

label {
    margin-bottom: 0.5em;
}

input, textarea {
    margin-bottom: 1em;
    padding: 0.5em;
    border: 1px solid #ccc;
    border-radius: 4px;
}

button {
    padding: 0.5em;
    background-color: #4CAF50;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

button:hover {
    background-color: #45a049;
}

ul {
    list-style-type: none;
    padding: 0;
}

li {
    padding: 1em;
    border: 1px solid #ccc;
    margin-bottom: 0.5em;
    border-radius: 4px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

li button {
    padding: 0.5em;
    background-color: #e74c3c;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

li button:hover {
    background-color: #c0392b;
}document.addEventListener("DOMContentLoaded", () => {
    const reportForm = document.getElementById("report-form");
    const reportList = document.getElementById("report-list");

    reportForm.addEventListener("submit", (e) => {
        e.preventDefault();

        const title = document.getElementById("title").value;
        const description = document.getElementById("description").value;

        addReport(title, description);
        reportForm.reset();
    });

    function addReport(title, description) {
        const li = document.createElement("li");

        const reportTitle = document.createElement("span");
        reportTitle.textContent = title;

        const reportDescription = document.createElement("span");
        reportDescription.textContent = description;

        const deleteButton = document.createElement("button");
        deleteButton.textContent = "Supprimer";
        deleteButton.addEventListener("click", () => {
            reportList.removeChild(li);
        });

        li.appendChild(reportTitle);
        li.appendChild(reportDescription);
        li.appendChild(deleteButton);

        reportList.appendChild(li);
    }git init
    git add .
    git remote add origin https://github.com/USERNAME/REPOSITORY_NAME.git
    git push -u origin main
    git push -u origin main
