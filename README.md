Game Link :
https://esrasisik.github.io/geogame/

GeoGame Project Report

Advanced JS Library Used in My Project: Leaflet.js
In the GeoGame project, I used the Leaflet.js library to create interactive maps. Leaflet.js is a lightweight and powerful mapping library that enabled me to visualize the geographical locations of cities. I used it as follows:

I initially focused the map on the center of Turkey (Ankara):

const map = L.map(mapElement).setView([39.9334, 32.8597], 6);
I dynamically added markers to show the locations of cities to the user:

L.marker(currentCity.coords).addTo(map);
Thanks to this library, the game became more interactive and fun for users.

Event Handlers Used in My Project
I used three important event listeners in my project:

Game Start:
When the user clicks the "Start Game" button, the game resets and a new city is loaded:

startButton.addEventListener('click', startGame);
Answer Checking:
When the user clicks the "Submit Answer" button, a function is executed to check the answer entered by the user:

submitButton.addEventListener('click', checkAnswer);
Timer:
The timer monitors the time during the game and ends the game when the time runs out:

timerInterval = setInterval(() => { ... }, 1000);
These event listeners provide the core functionality of the game.

Use of Closure
A closure is an inner function that retains access to the outer function’s variables. In the GeoGame project, I used a closure within the loadRandomCity function. For example:

The currentCity variable works as a closure and retains the city information until the next city is loaded:

function loadRandomCity(map) {
    const randomIndex = Math.floor(Math.random() * cities.length);
    currentCity = cities[randomIndex]; // Works as a closure
}
This structure simplified variable management and made the code more organized.

What I Learned from Artificial Intelligence
While creating this project, I utilized AI tools (such as ChatGPT) to assist in several areas, particularly:

Leaflet.js Usage: How to dynamically create maps and add markers.
Closure Structure: How to use closures to manage variables within the game.
General JavaScript Logic: Practical suggestions on event listeners and DOM manipulation.
I documented my learning process by including the URL of this conversation in my report.

Interaction with the DOM
DOM manipulation played a crucial role in keeping the user interface up-to-date. For example:

Showing Questions:
questionElement.textContent = currentCity.question;
Updating Score and Lives:

scoreElement.textContent = score;
livesElement.textContent = lives;
These methods allowed me to provide real-time feedback to the user.

Game Mechanics
GeoGame offers an engaging and interactive experience for users with the following features:

Random cities are selected, and a new question is asked each round.
The user earns points for correct answers and loses lives for incorrect ones.
The map dynamically displays the locations of cities, enhancing the game’s realism.
A time limit increases the sense of competition.
Use of Git
I used Git regularly throughout the development process to document each step. Below are some example commit messages:

Added basic game structure
Implemented score and lives tracking
Integrated Leaflet.js for map functionality
This method helped me track the progress of my code more systematically.

Conclusion: This project helped me enhance my skills in JavaScript, Leaflet.js, and DOM manipulation technologies. It also taught me the nuances of designing a game that enhances user interaction.

Through this process, I reinforced my software development skills using advanced JavaScript features such as event listeners and closures. By integrating an external library like Leaflet.js, I gained expertise in map-based applications. Additionally, working with AI tools sped up my problem-solving process and added a new dimension to my learning experience. The GeoGame project, with its technical aspects and focus on user experience, broadened my perspective on software design.

This experience laid the foundation for creating more effective and user-centered solutions in future projects.


