var xhr = new XMLHttpRequest(); // creates a XMLHttpRequest Object
xhr.onreadystatechange = function() { //Creates a callback function whenever there is a state change in the request
  if(xhr.readyState === 4) { //Checks for a readyState of '4', which means we have recieved everything of location we made request
    var employees = JSON.parse(xhr.responseText); //converts JSON into Javascript object and stores in variable 'employees'
    var statusHTML = '<ul class="bulleted">'; //Starts an 'ul' with a class, 'bullteted' connected to a css file not listed here
    for (var i=0; i < employees.length; i += 1) { //For loop cycling through the Javascript object 'employees'
      if(employees[i].inoffice === true) { //if employee is in office...
        statusHTML += '<li class="in">'; //Creates li with class, 'in'
      } else {
        statusHTML += '<li class="out">'; //otherwise Creates li with class, 'out'
      }
      statusHTML += employees[i].name;
      statusHTML += '</li>';
    }
    statusHTML += '</ul>';
    document.getElementById('employeeList').innerHTML = statusHTML;
  }
};
xhr.open('GET', 'data/employees.json');
xhr.send();
