# all2<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>JKS Group Unified Dashboard</title>
<style>
  body {
    font-family: Arial, sans-serif;
    background: #f7fafc;
    margin: 0;
    color: #205081;
  }
  .header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: #e3effa;
    padding: 16px 36px;
    font-size: 1.12em;
    font-weight: 600;
    color: #2e6aa7;
    border-bottom: 3px solid #7fd0f0;
  }
  .main-menu {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 28px;
    margin: 20px auto 30px;
    width: 90%;
  }
  .menu-box {
    background: #f4fafe;
    border: 2px solid #85bbeb;
    border-radius: 10px;
    min-width: 180px;
    padding: 30px 20px;
    text-align: center;
    font-size: 1.1em;
    font-weight: 600;
    color: #205081;
    box-shadow: 0 2px 8px #dde8f9;
    cursor: pointer;
    transition: background 0.3s ease;
  }
  .menu-box:hover {
    background: #d0e6fb;
  }
  .section-container {
    max-width: 900px;
    margin: 0 auto 40px;
    background: #fff;
    border-radius: 10px;
    box-shadow: 0 3px 14px #d3d7dbcc;
    padding: 20px 30px 30px;
  }
  h2.section-title {
    color: #295bb6;
    text-align: center;
    margin-bottom: 20px;
    font-weight: 700;
    font-size: 1.5em;
  }
  .display-bar {
    margin: 20px auto 25px auto;
    width: 100%;
    text-align: center;
    border: 2px solid #5ba9d5;
    border-radius: 7px;
    background: #f6fdfe;
    padding: 17px 0;
    color: #284067;
    font-size: 1.15em;
    font-weight: 500;
  }
  .sections-grid {
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
    gap: 30px;
  }
  .box {
    background: #fcfdff;
    border: 2px solid #6eb7e7;
    border-radius: 11px;
    padding: 25px 20px 20px;
    min-width: 310px;
    max-width: 350px;
    box-shadow: 0 2px 14px #daeefd60;
  }
  .box-title {
    background: #479ede;
    color: #fff;
    font-size: 1.18em;
    font-weight: 600;
    padding: 10px 0;
    border-radius: 8px;
    text-align: center;
    margin-bottom: 18px;
  }
  ul {
    margin-left: 20px;
    padding-left: 15px;
    color: #273965;
    font-size: 1.03em;
  }
  ul li {
    margin-bottom: 6px;
  }
  .back-button {
    display: block;
    margin: 20px auto 0;
    background-color: #003f7d;
    border: none;
    color: white;
    padding: 12px 50px;
    border-radius: 12px;
    font-weight: 600;
    font-size: 1em;
    cursor: pointer;
    box-shadow: 0 2px 8px #5a95d6;
  }
  /* Job & Services Styles */
  .btn-group, .service-categories, .job-categories {
    display: flex;
    justify-content: center;
    gap: 20px;
    flex-wrap: wrap;
    margin-bottom: 20px;
  }
  .button {
    background: white;
    color: #0288d1;
    border: 3px solid #03a9f4;
    padding: 15px 30px;
    border-radius: 12px;
    font-weight: bold;
    font-size: 16px;
    cursor: pointer;
    box-shadow: 2px 2px 8px rgba(3,169,244,0.3);
    transition: background-color 0.3s ease, color 0.3s ease;
    text-align: center;
  }
  .button:hover {
    background: #03a9f4;
    color: white;
    box-shadow: 2px 2px 12px rgba(3,169,244,0.7);
  }
  input[type="text"] {
    display: block;
    margin: 0 auto 20px auto;
    padding: 8px;
    font-size: 16px;
    border: 2px solid #03a9f4;
    border-radius: 6px;
    width: 250px;
    transition: border-color 0.3s ease;
  }
  input[type="text"]:focus {
    border-color: #0288d1;
    outline: none;
  }
  .display-section {
    margin-top: 20px;
    padding: 15px;
    background-color: #f1f8ff;
    border: 1px solid #03a9f4;
    border-radius: 6px;
    color: #01579b;
  }
  /* Tours & Travel Styles */
  nav {
    background-color: #87ceeb;
    display: flex;
    justify-content: center;
    gap: 25px;
    padding: 12px 0;
    margin-bottom: 20px;
  }
  nav button {
    background-color: white;
    border: none;
    padding: 10px 22px;
    border-radius: 5px;
    color: #87ceeb;
    cursor: pointer;
    font-weight: bold;
    font-size: 14px;
  }
  nav button:hover, nav button.active {
    background-color: #b0e0ff;
    color: #235e84;
  }
  main.tours-main {
    background-color: white;
    border: 2px solid #87ceeb;
    padding: 20px;
    border-radius: 10px;
    max-width: 900px;
    margin: 0 auto 30px;
  }
  /* Courier & Ride Booking Styles */
  .tabs {
    display: flex;
    justify-content: center;
    margin-bottom: 15px;
    gap: 18px;
  }
  .tabs button {
    padding: 10px 25px;
    background: white;
    border: 2px solid #87ceeb;
    border-radius: 6px;
    cursor: pointer;
    color: #87ceeb;
    font-weight: bold;
  }
  .tabs button.active, .tabs button:hover {
    background: #87ceeb;
    color: white;
  }
  .tab-section {
    display: none;
    margin-top: 15px;
  }
  .tab-section.active {
    display: block;
  }
  label {
    display: block;
    margin-top: 15px;
    font-weight: bold;
  }
  select, input[type="radio"] {
    margin-right: 6px;
  }
  .vehicle-options label {
    margin-right: 12px;
    font-weight: normal;
  }
</style>
</head>
<body>

<div class="header">
  <span>Profile</span>
  <span>Add Cash</span>
</div>

<div class="main-menu">
  <div class="menu-box" onclick="showSection('dashboard')">Dashboard Home</div>
  <div class="menu-box" onclick="showSection('loansInsurance')">Loans & Insurance</div>
  <div class="menu-box" onclick="showSection('jobService')">Job Consultancy & Services</div>
  <div class="menu-box" onclick="showSection('toursTravel')">Tours & Travels</div>
  <div class="menu-box" onclick="showSection('investmentBusiness')">Investments & Business</div>
  <div class="menu-box" onclick="showSection('courierRide')">Courier & Ride Booking</div>
  <div class="menu-box" onclick="showSection('eventsCatering')">Events & Catering</div>
</div>

<!-- Dashboard Section -->
<div id="dashboard" class="section-container">
  <h2 class="section-title">JKS Group Dashboard</h2>
  <div style="text-align:center; font-size:1.2em; font-weight: 500; color:#316796; padding: 25px 0; border: 2px solid #7fd0f0; border-radius: 8px; max-width:700px; margin:0 auto 20px;">
    Add (or) product display
  </div>
  <div class="sections-grid">
    <div class="box">My E-commerce</div>
    <div class="box">My Event & Catering</div>
    <div class="box">My Courier & My Riders</div>
    <div class="box">My Job Consultancy & My Services</div>
    <div class="box">Recharge & Pay Bills</div>
    <div class="box">Tours & My Travels</div>
    <div class="box">Real Estate & Construction</div>
    <div class="box">Investments & Business</div>
    <div class="box">My Franchise & My Micro Money</div>
    <div class="box">My Loans & My Insurance</div>
    <div class="box">My Games & My Entertainment</div>
  </div>
</div>

<!-- Loans & Insurance Section -->
<div id="loansInsurance" class="section-container" style="display:none;">
  <h2 class="section-title">Loans & Insurance</h2>
  <div class="display-bar">add display</div>
  <div class="sections-grid">
    <div class="box">
      <div class="box-title">Loans</div>
      <ul>
        <li>Loan</li>
        <li>Car</li>
        <li>Bike</li>
        <li>House</li>
        <li>Personal</li>
        <li>Business</li>
        <li>etc</li>
      </ul>
    </div>
    <div class="box">
      <div class="box-title">Insurance</div>
      <ul>
        <li>Health</li>
        <li>Mobile</li>
        <li>Car</li>
        <li>Bike</li>
        <li>etc</li>
      </ul>
    </div>
  </div>
</div>

<!-- Job Consultancy & Services Section -->
<div id="jobService" class="section-container" style="display:none;">

  <h2 class="section-title">Job Consultancy & Services</h2>

  <div class="btn-group" id="mainJobServiceButtons">
    <div class="button" onclick="showJobServiceSubSection('jobSection')">Job</div>
    <div class="button" onclick="showJobServiceSubSection('serviceSection')">Service</div>
  </div>

  <div id="jobSection" style="display:none;">
    <h3 style="text-align:center; color:#0277bd;">Job Categories</h3>
    <div class="job-categories">
      <div class="button">mt app Job</div>
      <div class="button">Local</div>
      <div class="button">non-Local</div>
      <div class="button">All</div>
    </div>
    <button class="back-button" onclick="backToJobServiceMain()">Back</button>
  </div>

  <div id="serviceSection" style="display:none;">
    <h3 style="text-align:center; color:#0277bd;">Service Locations & Types</h3>
    <label for="locationInput">Enter Location:</label>
    <input type="text" id="locationInput" placeholder="Type location" />
    <div class="service-categories">
      <div class="button" onclick="toggleDisplaySection('pgHostel')">PG / Hostel</div>
      <div class="button" onclick="toggleDisplaySection('rentedRoom')">Rented Room</div>
      <div class="button" onclick="toggleDisplaySection('teachingCenter')">Teaching Center</div>
    </div>
    <div class="display-section" id="pgHostel" style="display:none;">
      <h4>PG / Hostel Display</h4>
      <p>Display listings for PG / Hostel in the selected location.</p>
    </div>
    <div class="display-section" id="rentedRoom" style="display:none;">
      <h4>Rented Room Display</h4>
      <p>Display listings for Rented Rooms in the selected location.</p>
    </div>
    <div class="display-section" id="teachingCenter" style="display:none;">
      <h4>Teaching Center Display</h4>
      <p>Display listings for Teaching Centers in the selected location.</p>
    </div>
    <button class="back-button" onclick="backToJobServiceMain()">Back</button>
  </div>

</div>

<!-- Tours & Travel Section -->
<div id="toursTravel" class="section-container" style="display:none;">
  <h2 class="section-title">Tours and Travel</h2>

  <nav>
    <button onclick="showTourSection('tours')" class="active">Tours</button>
    <button onclick="showTourSection('rooms')">Rooms (Homestay)</button>
    <button onclick="showTourSection('travel')">Travel</button>
  </nav>

  <main class="tours-main">
    <section id="tours">
      <h3>My Tours</h3>
      <p>Display planned tours here.</p>
      <h4>Regular Tours & Packages</h4>
      <ul>
        <li>Kerala</li>
        <li>Goa</li>
        <li>Mumbai</li>
        <li>Others...</li>
      </ul>
    </section>
    <section id="rooms" style="display:none;">
      <h3>Rooms (Homestay)</h3>
      <p>Location-based rooms display here.</p>
    </section>
    <section id="travel" style="display:none;">
      <h3>Travel</h3>
      <h4>Vehicles</h4>
      <ul>
        <li>Car</li>
        <li>Van</li>
        <li>Volvo Bus</li>
        <li>Mini Bus</li>
      </ul>
      <h4>Tickets</h4>
      <ul>
        <li>Train</li>
        <li>Bus</li>
        <li>Flight</li>
        <li>Others...</li>
      </ul>
    </section>
  </main>
</div>

<!-- Investments & Business Section -->
<div id="investmentBusiness" class="section-container" style="display:none;">
  <h2 class="section-title">Investments & Business</h2>
  <div class="display-bar">Add display</div>
  <div class="sections-grid">
    <div class="box">
      <div class="box-title">Investment</div>
      <p style="color:#223559; margin-left:10px;">
        &darr; open<br />
        - Real Estate<br />
        - Add<br />
        - Events<br />
        - Etc
      </p>
    </div>
    <div class="box">
      <div class="box-title">Business</div>
      <p style="color:#223559; margin-left:10px;">
        &darr; open<br />
        - Second Hand Car<br />
        - Second Hand Bike<br />
        - Second Hand Mobile
      </p>
      <div style="text-align:center; margin-top:20px;">
        <button style="background:#285b88; color:#fff; border:none; margin-right: 15px; padding: 11px 34px; border-radius: 8px; font-weight: 600; font-size: 1.04em; cursor:pointer;">
          SELL
        </button>
        <button style="background:#285b88; color:#fff; border:none; padding: 11px 34px; border-radius: 8px; font-weight: 600; font-size: 1.04em; cursor:pointer;">
          BUY
        </button>
      </div>
    </div>
  </div>
</div>

<!-- Courier & Ride Booking Section -->
<div id="courierRide" class="section-container" style="display:none;">
  <h2 class="section-title">My Courier Delivery & Ride Booking</h2>
  <div class="tabs">
    <button id="courierBtn" class="active">Courier</button>
    <button id="rideBtn">Ride Booking</button>
    <button id="rentBtn">Rental Vehicle</button>
  </div>

  <div id="courier" class="tab-section active">
    <label>Choose Location:</label>
    <select id="courierLocation">
      <option value="send">Send</option>
      <option value="receive">Receive</option>
    </select>

    <label>Vehicle Type:</label>
    <div class="vehicle-options">
      <label><input type="radio" name="courierVehicle" value="bike" checked /> Bike</label>
      <label><input type="radio" name="courierVehicle" value="auto" /> Auto</label>
      <label><input type="radio" name="courierVehicle" value="car" /> Car</label>
      <label><input type="radio" name="courierVehicle" value="miniauto" /> Mini Auto</label>
      <label><input type="radio" name="courierVehicle" value="lorry" /> Lorry</label>
    </div>
  </div>

  <div id="ride" class="tab-section">
    <label>Select Ride Type:</label>
    <div class="vehicle-options">
      <label><input type="radio" name="rideType" value="bike" checked /> Bike</label>
      <label><input type="radio" name="rideType" value="auto" /> Auto</label>
      <label><input type="radio" name="rideType" value="car" /> Car</label>
    </div>
  </div>

  <div id="rent" class="tab-section">
    <label>Select Mode:</label>
    <div class="vehicle-options">
      <label><input type="radio" name="rentMode" value="self" checked /> Self</label>
      <label><input type="radio" name="rentMode" value="driver" /> With Driver</label>
    </div>

    <div id="selfVehicleOptions">
      <label>Choose Vehicle:</label>
      <div class="vehicle-options">
        <label><input type="radio" name="selfVehicle" value="bike" checked /> Bike</label>
        <label><input type="radio" name="selfVehicle" value="car" /> Car</label>
        <label><input type="radio" name="selfVehicle" value="auto" /> Auto</label>
      </div>
    </div>

    <div id="driverVehicleOptions" style="display:none;">
      <label>Choose Vehicle:</label>
      <div class="vehicle-options">
        <label><input type="radio" name="driverVehicle" value="bike" /> Bike</label>
        <label><input type="radio" name="driverVehicle" value="car" /> Car</label>
        <label><input type="radio" name="driverVehicle" value="auto" /> Auto</label>
        <label><input type="radio" name="driverVehicle" value="bolero" /> Bolero</label>
        <label><input type="radio" name="driverVehicle" value="volvo" /> Volvo</label>
        <label><input type="radio" name="driverVehicle" value="jeep" /> Jeep</label>
      </div>
    </div>
  </div>
</div>

<!-- Events & Catering Section -->
<div id="eventsCatering" class="section-container" style="display:none;">
  <h2 class="section-title">Event & Catering Services</h2>
  <div class="display-bar">add display</div>
  <div style="text-align:center; margin-bottom: 25px;">
    <span style="background: #468ac9; color: white; padding: 14px 40px; border-radius: 7px; font-size: 1.1em; font-weight: 600; margin: 0 10px; display: inline-block; box-shadow: 0 2px 8px #e0e7ee77; cursor:default;">
      Package
    </span>
    <span style="background: #468ac9; color: white; padding: 14px 40px; border-radius: 7px; font-size: 1.1em; font-weight: 600; margin: 0 10px; display: inline-block; box-shadow: 0 2px 8px #e0e7ee77; cursor:default;">
      Customized
    </span>
    <span style="background: #468ac9; color: white; padding: 14px 40px; border-radius: 7px; font-size: 1.1em; font-weight: 600; margin: 0 10px; display: inline-block; box-shadow: 0 2px 8px #e0e7ee77; cursor:default;">
      Premium
    </span>
  </div>
  <div>
    <div style="display:flex; justify-content:center; gap: 35px; margin-bottom: 20px; flex-wrap: wrap;">
      <div style="background:#f3f4fa; border: 2px solid #3399cc; border-radius: 10px; min-width: 145px; padding: 15px 10px; text-align:center; font-size:1em; font-weight:500; color:#2a4c8d;">
        Decoration<br><small>[garlands & accessories]</small>
      </div>
      <div style="background:#f3f4fa; border: 2px solid #3399cc; border-radius: 10px; min-width: 145px; padding: 15px 10px; text-align:center; font-size:1em; font-weight:500; color:#2a4c8d;">
        Catering
      </div>
      <div style="background:#f3f4fa; border: 2px solid #3399cc; border-radius: 10px; min-width: 145px; padding: 15px 10px; text-align:center; font-size:1em; font-weight:500; color:#2a4c8d;">
        Conventions
      </div>
      <div style="background:#f3f4fa; border: 2px solid #3399cc; border-radius: 10px; min-width: 145px; padding: 15px 10px; text-align:center; font-size:1em; font-weight:500; color:#2a4c8d;">
        Photography & Videography
      </div>
    </div>
    <div style="display:flex; justify-content:center; gap: 35px; margin-bottom: 20px; flex-wrap: wrap;">
      <div style="background:#f3f4fa; border: 2px solid #3399cc; border-radius: 10px; min-width: 145px; padding: 15px 10px; text-align:center; font-size:1em; font-weight:500; color:#2a4c8d;">
        Anchor & Actors
      </div>
      <div style="background:#f3f4fa; border: 2px solid #3399cc; border-radius: 10px; min-width: 145px; padding: 15px 10px; text-align:center; font-size:1em; font-weight:500; color:#2a4c8d;">
        DJ & Dance & Singers
      </div>
      <div style="background:#f3f4fa; border: 2px solid #3399cc; border-radius: 10px; min-width: 145px; padding: 15px 10px; text-align:center; font-size:1em; font-weight:500; color:#2a4c8d;">
        Guest House [rooms]
      </div>
      <div style="background:#f3f4fa; border: 2px solid #3399cc; border-radius: 10px; min-width: 145px; padding: 15px 10px; text-align:center; font-size:1em; font-weight:500; color:#2a4c8d;">
        Chocolate & Cake
      </div>
    </div>
    <div style="display:flex; justify-content:center; gap: 35px; flex-wrap: wrap;">
      <div style="background:#f3f4fa; border: 2px solid #3399cc; border-radius: 10px; min-width: 145px; padding: 15px 10px; text-align:center; font-size:1em; font-weight:500; color:#2a4c8d;">
        Games & Entertainment
      </div>
      <div style="background:#f3f4fa; border: 2px solid #3399cc; border-radius: 10px; min-width: 145px; padding: 15px 10px; text-align:center; font-size:1em; font-weight:500; color:#2a4c8d;">
        Jewellery
      </div>
      <div style="background:#f3f4fa; border: 2px solid #3399cc; border-radius: 10px; min-width: 145px; padding: 15px 10px; text-align:center; font-size:1em; font-weight:500; color:#2a4c8d;">
        Invitation Cards
      </div>
      <div style="background:#f3f4fa; border: 2px solid #3399cc; border-radius: 10px; min-width: 145px; padding: 15px 10px; text-align:center; font-size:1em; font-weight:500; color:#2a4c8d;">
        Vehicles
      </div>
      <div style="background:#f3f4fa; border: 2px solid #3399cc; border-radius: 10px; min-width: 145px; padding: 15px 10px; text-align:center; font-size:1em; font-weight:500; color:#2a4c8d;">
        Return Gifts
      </div>
    </div>
  </div>
</div>

<script>
  function showSection(id) {
    document.querySelectorAll('.section-container').forEach(section => {
      section.style.display = 'none';
    });
    document.getElementById(id).style.display = 'block';
    if (id === 'toursTravel') {
      showTourSection('tours');
    } else if (id === 'jobService') {
      backToJobServiceMain();
    } else if (id === 'courierRide') {
      activateCourierTabs('courierBtn', 'courier');
    }
  }

  // Job Service Subsections
  function showJobServiceSubSection(id) {
    document.getElementById('mainJobServiceButtons').style.display = 'none';
    if(id === 'jobSection') {
      document.getElementById('jobSection').style.display = 'block';
      document.getElementById('serviceSection').style.display = 'none';
    } else {
      document.getElementById('jobSection').style.display = 'none';
      document.getElementById('serviceSection').style.display = 'block';
    }
  }
  function backToJobServiceMain() {
    document.getElementById('mainJobServiceButtons').style.display = 'flex';
    document.getElementById('jobSection').style.display = 'none';
    document.getElementById('serviceSection').style.display = 'none';
  }
  function toggleDisplaySection(id) {
    const el = document.getElementById(id);
    el.style.display = (el.style.display === 'block') ? 'none' : 'block';
  }

  // Tours & Travel nav
  function showTourSection(id) {
    const sections = ['tours', 'rooms', 'travel'];
    sections.forEach(s => {
      document.getElementById(s).style.display = (s === id) ? 'block' : 'none';
    });
    document.querySelectorAll('nav button').forEach(btn => btn.classList.remove('active'));
    event.target.classList.add('active');
  }

  // Courier & Ride Booking tabs
  const courierBtn = document.getElementById('courierBtn');
  const rideBtn = document.getElementById('rideBtn');
  const rentBtn = document.getElementById('rentBtn');
  const courierSection = document.getElementById('courier');
  const rideSection = document.getElementById('ride');
  const rentSection = document.getElementById('rent');

  courierBtn.addEventListener('click', () => activateCourierTabs('courierBtn', 'courier'));
  rideBtn.addEventListener('click', () => activateCourierTabs('rideBtn', 'ride'));
  rentBtn.addEventListener('click', () => activateCourierTabs('rentBtn', 'rent'));

  function activateCourierTabs(btnId, sectionId) {
    [courierBtn, rideBtn, rentBtn].forEach(btn => btn.classList.remove('active'));
    document.getElementById(btnId).classList.add('active');
    [courierSection, rideSection, rentSection].forEach(sec => sec.classList.remove('active'));
    document.getElementById(sectionId).classList.add('active');
  }

  // Rental Vehicle mode toggle in Courier section
  const rentModeRadios = document.getElementsByName('rentMode');
  rentModeRadios.forEach(radio => {
    radio.addEventListener('change', () => {
      const selfVehicle = document.getElementById('selfVehicleOptions');
      const driverVehicle = document.getElementById('driverVehicleOptions');
      if(radio.value === 'self') {
        selfVehicle.style.display = 'block';
        driverVehicle.style.display = 'none';
      } else {
        selfVehicle.style.display = 'none';
        driverVehicle.style.display = 'block';
      }
    });
  });

  // Show initial section
  showSection('dashboard');
</script>

</body>
</html>
