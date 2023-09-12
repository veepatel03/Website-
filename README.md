# Website-
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Health & Fitness Planner</title>
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <header>
        <h1>Health & Fitness Planner</h1>
    </header>

    <nav>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#planner">Fitness Planner</a></li>
            <li><a href="#gallery">Gallery</a></li>
        </ul>
    </nav>

    <section id="home">
        <h2>Welcome to the Health & Fitness Website</h2>
        <p>Start your fitness journey with us!</p>
    </section>
    <section id="planner">
        <h2>Fitness Planner</h2>
    
        <form id="exerciseForm">
            <label for="goal">Your Fitness Goal:</label>
            <input type="text" id="goal" placeholder="e.g., Lose 10 lbs, Run 2k" required>
            <br>
    
            <label for="completionDate">Target Date to Achieve Goal:</label>
            <input type="date" id="completionDate" required>
            <br>
    
            <label for="exercise">Choose an exercise:</label>
            <select name="exercise" id="exercise">
                <option value="cardio">Cardio</option>
                <option value="lifting">Lifting</option>
                <option value="yoga">Yoga</option>
                <option value="cycling">Cycling</option>
                <option value="pilates">Pilates</option>
                <option value="swimming">Swimming</option>
                <option value="boxing">Boxing</option>
                <option value="walking">Walking</option>
            </select>
            <br>
            
            <label for="duration">Duration (minutes):</label>
            <input type="number" id="duration" name="duration">
            <br>
            
            <input type="button" value="Add to Planner" onclick="addToPlanner()">
        </form>
    
        <h3>My Fitness Plan Schedule:</h3>
        <ul id="exerciseList"></ul>
    </section>
        </form>

    <section id="gallery">
        <h2>Gallery</h2>
        <img src="image1.jpeg" alt="Image 1" class="gallery-img">
        <img src="image5.1.jpeg" alt="Image 5.1" class="gallery-img">
        <img src="image2.jpeg" alt="Image 2" class="gallery-img">
        <img src="image3.jpeg" alt="Image 3" class="gallery-img">
        <img src="image6.jpeg" alt="Image 6" class="gallery-img">
        <img src="image4.jpeg" alt="Image 4" class="gallery-img">
        <!-- Add more images as needed -->
    </section>

    <footer>
        <p>© 2023 Health & Fitness Planner</p>
    </footer>

    <script>
        function addToPlanner() {
            var exerciseDropdown = document.getElementById('exercise');
            var durationInput = document.getElementById('duration');

            var selectedExercise = exerciseDropdown.options[exerciseDropdown.selectedIndex].text;
            var duration = durationInput.value;

            var listItem = document.createElement('li');
            listItem.textContent = `${selectedExercise} for ${duration} minutes`;

            document.getElementById('exerciseList').appendChild(listItem);
        }
    </script>
</body>

</html>









