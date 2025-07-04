<html>
<head>
  <title>Clinic Management System</title>
  <style>
    body { font-family: Arial; padding: 20px; }
    table { width: 100%; border-collapse: collapse; margin-top: 20px; }
    table, th, td { border: 1px solid black; }
    th, td { padding: 10px; text-align: left; }
  </style>
</head>
<body>
  <h1>Patient Registration</h1>
  <form id="patientForm">
    Name: <input type="text" id="name" required><br><br>
    Age: <input type="number" id="age" required><br><br>
    Contact: <input type="text" id="contact" required><br><br>
    <button type="submit">Add Patient</button>
  </form>

  <h2>Patient List</h2>
  <table>
    <thead>
      <tr>
        <th>Name</th><th>Age</th><th>Contact</th>
      </tr>
    </thead>
    <tbody id="patientList"></tbody>
  </table>

  <script>
    document.getElementById("patientForm").addEventListener("submit", function(e) {
      e.preventDefault();
      const name = document.getElementById("name").value;
      const age = document.getElementById("age").value;
      const contact = document.getElementById("contact").value;

      const table = document.getElementById("patientList");
      const row = table.insertRow();
      row.insertCell(0).textContent = name;
      row.insertCell(1).textContent = age;
      row.insertCell(2).textContent = contact;

      document.getElementById("patientForm").reset();
    });
  </script>
</body>
</html>

