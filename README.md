# USERNAME-
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>User Registration</title>
</head>
<body>

    <h2>User Registration</h2>

    <form id="registrationForm" onsubmit="displayEntries(event)">
        <label for="name">Name:</label>
        <input type="text" id="name" name="name" required><br>

        <label for="email">Email:</label>
        <input type="email" id="email" name="email" required><br>

        <label for="password">Password:</label>
        <input type="password" id="password" name="password" required><br>

        <label for="dob">Date of Birth:</label>
        <input type="date" id="dob" name="dob" required><br>

        <label for="terms">Accept Terms and Conditions:</label>
        <input type="checkbox" id="terms" name="terms" required><br>

        <button type="submit">Submit</button>
    </form>

    <div id="displayEntries"></div>

    <script>
        function displayEntries(event) {
            event.preventDefault();
            
            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            const password = document.getElementById('password').value;
            const dob = document.getElementById('dob').value;
            const terms = document.getElementById('terms').checked;

            const displayEntriesDiv = document.getElementById('displayEntries');
            displayEntriesDiv.innerHTML = `
                <h3>Entered Information:</h3>
                <p><strong>Name:</strong> ${name}</p>
                <p><strong>Email:</strong> ${email}</p>
                <p><strong>Password:</strong> ${password}</p>
                <p><strong>Date of Birth:</strong> ${dob}</p>
                <p><strong>Accepted Terms and Conditions:</strong> ${terms ? 'Yes' : 'No'}</p>
            `;
        }
    </script>

</body>
</html>

