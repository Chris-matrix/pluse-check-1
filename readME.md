Project Task: 

[]Embed your css into your HTML page 
[]Create an HTML header section and add todo comments for the future implementation of the project 
[]Create footer that holds the temporary links for your social media handles that we will be adding as the project progresses
[]Create a main section that will hold the projects list 
[]In the main section nest an image tag and anchor tag for each image
[]Add the required and optional attributes to the image tag 
[]Add the class attribute to all element 
[]Center the images on the page so that there’s an even amount of space from the top, bottom, left and right side of the page 
[]Comment the code to explain how you are thinking about adding new or existing elements 
[]Add id and class attributes names that are useful in helping to your peers so that they will be able to provide feedback
Next Level Flex: 
[]Add comments that can be used to enhance the current state of the HTML page. For example, JSDoc Comment placeholder functionality that can be picked up by other developers.  
[]Target level 12 indicators on the concept rubric 


<html>
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width" />
    <title>Replit</title>
    <link href="style.css" rel="stylesheet" type="text/css" />
    <style>
      /* Table UI format  */
      th, td {
        border: 1px outset;
        width: 100%;
      }
      /* Launchpad Philly Logo */
      img {
        width: 200px;
        height: 150px;
        background-color: lightblue;
        border-radius: 5%;
      }
      /* Total earnings and Program form  */
      .new-program-form, .calcu-form {
        border: 1px dashed;
        display: block;
        width: 200px;
        margin: auto;
        padding: 2%;
      }
      /* Total earnings calcuation form  */
       .calcu-form {
        width: 400px;
        border: 2px solid;
      }
       .calcu-form > input {
        width: 75px;
        border: none;
        border-bottom: 2px solid;
      }
      label {
        display: block;
        margin-bottom: 5px
        font-weight: bold;
      }
      input {
        box-sizing: border-box;
        padding: 3px;
        margin: 5%;
      }
       /* Button load state  */
      .program-btn, .calcu-btn{
        color: white;
        background-color: grey;
        height: 75%;
        width: 75%;
        transition: background-color 1s, height 1s, width 1s;
        /* transition: all 1s; */
      }
      /*  Results UI elememt from the calculation */
      .total-earnings{
        color: green;
        font-size: 26px;
        text-align: center;
      }
       /* Create the layout for the form  */
      .grid-frame{
        display:inline-grid;
        grid-template-columns: 35% auto;
        padding: 10px;
      }
      /*  Hover effect for buttons */
      .calcu-btn:hover, .program-btn:hover{
        background-color: limegreen;
        width: 100%;
        height: 100%;
        color: whitesmoke
      }
      footer {
        background-color: lightblue;
        padding: 10px;
        text-align: center;
        color: whitesmoke;
      }
    </style>
    <script>
      console.log("Hello world!");
    </script>
  </head>
  <!-- 1. Add a comment for the logo, then move the Launchpad below the closing head tag
     2. Add width and height attributes
     3. Add a background color hexadecimal
     4. Add a comment "Table styles" and style the table headers using `th` & `td` tags
  -->
  <img
    src="https://www.yugioh.com"
    alt="lp-small-logo"
  />
  <body>
    <!-- Launchpad Program App   -->
    <main>
      <h1>Learning HTML/CSS & JavaScript</h1>
      <hr />
      <p >
        The web foundation is built on top of
        <strong><i>HTML, CSS and JavaScript</i></strong
        >.
      </p>
      <section>
        <aside class="card title">Foundations</aside>
        <aside class="card title">Launchpad 101</aside>
        <aside class="card title">Liftoff </aside>
      </section>
      <!-- HTML Table   -->
      <table>
        <!-- First Column Program Names -->
        <tr>
          <th>Program</th>
          <th>Duration</th>
          <th>Earning Potential</th>
        </tr>
        <!-- Second Column Duration -->
        <tr>
          <td><span>&#128708;</span> Foundations</td>
          <td>10</td>
          <td>1,500$</td>
        </tr>
        <!-- Third Column Earning Potential -->
        <tr>
          <td><span>&#128690;</span> Launchpad 101</td>
          <td>20</td>
          <td>3,000$</td>
        </tr>
        <!-- Fourth row -->
        <tr>
          <td><span>&#128747;</span>Liftoff</td>
          <td>30</td>
          <td>12,000$</td>
        </tr>
      </table>
      <section>
        <br />
        <!-- Part 1: Add a new program to the table  -->
        <!--Part 2: wrap a form element around the new program update () -->
        <form class="new-program-form">
          <label for="program">Program:</label>
          <input type="text" id="program" name="program" />
          <label for="duration">Duration:</label>
          <input type="text" id="duration" name="duration" />
          <label for="earnings">Potential Earnings:</label>
          <input type="text" id="earnings" name="earnings" />
          <!-- <input type="submit" value="Add New Program" /> -->
          <button class="program-btn">Add New Program</button>
        </form>
      </section>
      <!-- Part1: Module 4 Calculate the total earnings  -->
      <!-- Part 2: Wrapp a form element around the calculator  -->
      <aside>
        <h2>Launchpad Total Earning Calculator</h2>
        <form class="calcu-form grid-frame">
          <label for="foundations">Foundations </label>
          <input type="number" id="lp-fds" name="foundations" />
          <label for="Launchpad101">Launchpad 101: </label>
          <input type="number" id="lp-101" name="Launchpad101" />
          <label for="Liftoff">Liftoff: </label>
          <input type="number" id="liftoff" name="liftoff" />
          <button class="calcu-btn">Calculate</button>
          <aside class="total-earnings">
            <span id="result" class="result">$0</span>
          </aside>
          <!-- <p id="result"></p> -->
        </form>
      </aside>
      <!-- Date Slider, this will be removed in Concept 7. -->
      <!-- <section>
        <label for="date">Select a date:</label>
        <input type="date" id="date" name="date" />
        <input type="range" min="0" max="100" value="75">
      </section> -->
    </main>
    <hr />
    <footer>
      <p>&copy; Launchpad Philly. All Rights Reserved.</p>
      <p><a href="sign-up-form.html">Sign up for our news letter</a></p>
      <p><a href="contact-us-form.html">Contact Us</a></p>
    </footer>
    <script type="module" src="script.js"></script>
  </body>
</html>