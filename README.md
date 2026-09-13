<img width="1280" height="640" alt="git (1)" src="https://github.com/user-attachments/assets/8920b256-2ba8-4988-b824-5351134eb4bd" />

# The Balarama Gazette 🎯

## Basic Details
### Team Name: Fortons

### Team Members
- Team Lead: Rayhan KN - SOE CUSAT
- Member 2: Sreedhar Hari - SOE CUSAT

### Project Description
The Balarama Gazette: A Balarama-inspired online news reader where each page is locked behind a riddle or puzzle featuring Balarama characters. The puzzles get harder with every page, making reading the news progressively more frustrating by design.

### The Problem (that doesn't exist)
Reading the news today is way too quick and painless — readers get informed without any struggle, suspense, or sense of accomplishment. The Balarama Gazette proudly fixes this problem that nobody asked for, turning effortless news reading into a needlessly difficult ordeal.

### The Solution (that nobody asked for)
The Balarama Gazette locks every news page behind a riddle or puzzle featuring Balarama characters, with difficulty escalating page by page ensuring readers earn every headline through unnecessary struggle instead of just, you know, reading it. Features include Connect-the-Dots, Malayalam Jumble Words, Luttappi's Jokebox, and an AI Hand-Tracking Cricket Game!

## Technical Details
### Technologies/Components Used
For Software:
- **Languages used**: HTML, CSS, JS, PYTHON
- **Frameworks/Libraries used**: MediaPipe Tasks Vision (for AI Hand Tracking in the Sports section)
- **Vanilla HTML5**: Standard HTML without any templating engines.
- **Vanilla CSS3**: Custom, hand-written CSS directly embedded in the HTML file (`<style>` tag) rather than using frameworks like Tailwind, Bootstrap, or Material UI.
- **Vanilla JavaScript**: The interactive functionality and animations are written using standard DOM APIs within the `<script>` tags, without relying on libraries like React, Vue, jQuery, or GSAP.
- **Tools used**: Git, GitHub, Python (for local HTTP testing server)

### Implementation
For Software:
1. Setup & Installation
Since the project was designed to be as lightweight and accessible as possible, we opted out of using heavy node modules or build steps (like Webpack or React).

Clone the Repository:
bash
git clone https://github.com/reyyhann77/the_balarama_gazzette.git
cd the_balarama_gazzette
Dependencies: No npm install is required. All external libraries (like Google MediaPipe) are fetched dynamically via CDN at runtime.
2. Development & Coding
Structure: Everything is housed inside a single monolithic index.html file containing the DOM structure, embedded <style> tags for CSS, and <script> tags for the game logic.
Layout: We used CSS Grid and Flexbox to build the responsive newspaper-style columns and puzzle boards.
Game Mechanics Implementation:
Connect the Dots: Used the DOM API to track mouse/touch coordinates and dynamically generated SVG <path> elements to draw the connecting lines.
Jigsaw Puzzle: Implemented the native HTML5 Drag and Drop API, utilizing dragstart, dragover, and drop event listeners to snap pieces into a CSS Grid board.
Jumble Words: Used basic DOM manipulation to append and remove letter tiles between different flex containers, validating the text arrays on each click.
3. AI & Machine Learning Integration
Library: Imported HandLandmarker and FilesetResolver from the @mediapipe/tasks-vision module via unpkg CDN.
Camera Access: Used navigator.mediaDevices.getUserMedia() to prompt the user for webcam access and stream it to a hidden HTML <video> element.
Inference Loop: Set up a requestAnimationFrame loop that constantly feeds video frames to the MediaPipe model to extract 3D hand coordinates.
Custom Logic: Wrote a custom finger-counting algorithm that determines if exactly two fingers are raised (checking if finger tip Y-coordinates are higher than the PIP joint Y-coordinates).
4. Running & Testing locally
Because the webcam API and ES modules are restricted by browser CORS policies when opening files directly (via file://), the project must be run over a local web server.

Run Command:
bash
python3 -m http.server 8080
Access: Navigating to http://localhost:8080 allows the browser to properly load the AI models and request camera permissions.
5. Deployment
The project was deployed via Vercel as a static application (using the "Other" framework preset). Because it is purely vanilla HTML/JS, Vercel instantly hosts it without requiring any build commands.
4:59 PM

# Installation
1. Clone the repository to your local machine:
   ```bash
   git clone <your-repo-url>
   cd useless
   ```
2. No package installation is necessary as the project relies purely on vanilla JS and CDN imports!

# Run
1. Start a local HTTP server in the project directory (required for MediaPipe and modules to work due to CORS):
   ```bash
   python3 -m http.server 8080
   ```
2. Open your web browser and navigate to:
   ```
   http://localhost:8080
   ```

### Project Documentation
For Software:

# Screenshots
<img width="727" height="572" alt="Screenshot 2026-09-13 164810" src="https://github.com/user-attachments/assets/92e45cda-3f8a-45b1-b6c9-bc899fb52a70" />

<img width="1057" height="850" alt="image" src="https://github.com/user-attachments/assets/bc621007-81de-47ee-b0fb-7f707894c19c" />

<img width="742" height="848" alt="image" src="https://github.com/user-attachments/assets/b357c484-7c1e-4e79-b2e7-3648d178b83b" />
<img width="822" height="791" alt="image" src="https://github.com/user-attachments/assets/73499d66-c4f3-4049-877a-137a396b93d4" />
<img width="783" height="862" alt="image" src="https://github.com/user-attachments/assets/8e8cd488-5baa-47bd-84af-c2eee3f8a931" />
<img width="860" height="790" alt="image" src="https://github.com/user-attachments/assets/3cc174cf-fb6e-4a9d-a4df-f5b0ffdb0405" />
<img width="420" height="528" alt="image" src="https://github.com/user-attachments/assets/c6e8708d-5812-4ee7-ab99-63654aff948d" />
<img width="773" height="807" alt="image" src="https://github.com/user-attachments/assets/c08bb5ef-ee7d-470f-8aff-c1fec5156f1e" />


*The AI-Powered Cricket Game where you hold up 2 fingers to swing.*

![Classifieds]
*The highly satirical Classifieds section featuring vintage comics and characters.*

## Team Contributions
- **Rayhan KN**: Concept generation, layout design, content curation (riddles, news, and jokes), UI aesthetics, Frontend & Backend.
- **Sreedhar Hari**: Core frontend development, MediaPipe AI integration, logic for puzzles (Connect-the-dots, Jigsaw, Quiz), debugging, Frontend & UI/UX.

---
Made with ❤️ at TinkerHub Useless Projects 

![Static Badge](https://img.shields.io/badge/TinkerHub-24?color=%23000000&link=https%3A%2F%2Fwww.tinkerhub.org%2F)
![Static Badge](https://img.shields.io/badge/UselessProjects--26-26?link=https%3A%2F%2Ftinkerhub.org%2Fevents%2F1M8ORET9A1%2Fuseless-projects-3.0)
