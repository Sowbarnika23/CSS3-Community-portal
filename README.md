# CSS3-Community-portal
/*html code*/
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Local Community Event Portal</title>

  <!-- External CSS -->
  <link rel="stylesheet" href="styles.css">

  <!-- Google Font -->
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">

  <!-- Internal CSS -->
  <style>
    /* Embedded Styles */
    body {
      background: #f5f5f5 url('images/background.jpg') no-repeat center center fixed;
      background-size: cover;
    }
  </style>
</head>
<body>

  <!-- Inline Style Example -->
  <h1 style="color: red;">Welcome to the Community Portal</h1>

  <!-- Header Section -->
  <header id="mainHeader">
    <nav>
      <ul class="navMenu">
        <li><a href="#">Home</a></li>
        <li><a href="#">Events</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>
  </header>

  <!-- Event Cards -->
  <section>
    <div class="eventCard">
      <h2>Music in the Park</h2>
      <h3>Enjoy Local Talent</h3>
      <p class="description">Join us for a free concert in the park featuring local bands. Bring a blanket and snacks!</p>
    </div>
    <div class="eventCard">
      <h2>Farmers Market</h2>
      <h3>Fresh & Organic</h3>
      <p class="description">Support local farmers and buy fresh produce every Saturday morning downtown.</p>
    </div>
  </section>

  <!-- Community Bulletin -->
  <section class="news">
    <h2>Community News</h2>
    <article>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin lacinia ante vel metus lacinia, sit amet laoreet nunc elementum. Aenean vitae volutpat ligula. Quisque nec arcu vitae sapien porttitor blandit.</p>
    </article>
  </section>

  <!-- Events Table -->
  <section>
    <h2>Upcoming Events</h2>
    <table>
      <tr>
        <th>Event</th>
        <th>Date</th>
        <th>Location</th>
      </tr>
      <tr>
        <td>Cleanup Drive</td>
        <td>June 5</td>
        <td>Main Street</td>
      </tr>
      <tr>
        <td>Summer Parade</td>
        <td>July 10</td>
        <td>Central Ave</td>
      </tr>
    </table>
  </section>

  <!-- Form Section -->
  <form>
    <label for="name">Name:</label>
    <input type="text" id="name" class="highlight">

    <label for="email">Email:</label>
    <input type="email" id="email">

    <input type="submit" class="cta-button" value="Register">
  </form>

</body>
</html>
/*css code*/
/* Global Reset */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* Body Styles */
body {
  font-family: 'Roboto', sans-serif;
  color: #333;
}

/* Header styles */
#mainHeader {
  background-color: rgba(0, 123, 255, 0.9);
  padding: 1em;
  text-align: center;
}

.navMenu {
  list-style-type: none;
  list-style-position: inside;
  display: flex;
  justify-content: center;
  gap: 20px;
}

.navMenu li {
  padding: 5px 10px;
}

.navMenu a:link,
.navMenu a:visited {
  color: white;
  text-decoration: none;
}

.navMenu a:hover {
  text-decoration: underline;
}

.navMenu a:active {
  color: #ffd700;
}

/* Event Card Styles */
.eventCard {
  border: 2px solid #ccc;
  margin: 20px;
  padding: 15px;
  background-color: #ffffffcc;
  outline: none;
}

/* Typography and Description Styling */
.description {
  font-size: 16px;
  font-style: italic;
  font-weight: 400;
  text-align: justify;
  text-transform: none;
  letter-spacing: 0.5px;
  line-height: 1.6;
}

/* Grouped Selector */
h3, p {
  color: #444;
}

/* Button Styling */
.cta-button {
  background-color: #007BFF;
  color: white;
  padding: 10px 20px;
  border: none;
  margin-top: 10px;
}

/* Table Styling */
table {
  width: 100%;
  border-collapse: collapse;
  margin: 20px 0;
  text-align: center;
}

th, td {
  border: 1px solid #aaa;
  padding: 10px;
  background-color: #f9f9f9;
}

/* Zebra Striping */
tr:nth-child(even) {
  background-color: #e0e0e0;
}

/* Column Layout */
.news article {
  column-count: 2;
  column-gap: 30px;
  column-rule: 1px solid gray;
  margin: 20px;
}

/* Highlight outline */
.highlight {
  outline: 2px dashed green;
}

/* Visibility example (not used in HTML directly, just for reference) */
.invisible {
  visibility: hidden;
}

.hidden {
  display: none;
}

/* Responsive Design */
@media screen and (max-width: 768px) {
  .navMenu {
    flex-direction: column;
    align-items: center;
  }

  body {
    font-size: 90%;
  }

  img, .eventCard {
    width: 90%;
  }
}
