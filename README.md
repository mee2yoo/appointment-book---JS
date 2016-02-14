# appointment-book---JS
Appointment book built in JS for a class project.

<script>
				
		var object1 = {};
		object1.firstName = "Stephen";
		object1.lastName = "Adams";
		object1.email = "contact@me.com";
		object1.time = new Date(10,15,1997,13);
		
		var object2 = {};
		object2.firstName = "Billy";
		object2.lastName = "Mills";
		object2.email = "like@me.com";
		object2.time = new Date(11,21,1998,15);
		
		var object3 = {};
		object3.firstName = "Mike";
		object3.lastName = "Smith";
		object3.email = "dontcall@me.com";
		object3.time = new Date(9,14,1999,14);
		
		var booking =[
		object1,
		object2,
		object3
		];
		
		function listAppointments(apptArray) {
		for(i = 0; i <apptArray.length; i++) {	
		printAppointment(apptArray[i]);
			}
		}
		window.onload=listAppointments(pastAppt),listAppointments(futureAppt);
		
		var pastAppt = [];
		var futureAppt = [];
						 
		function takeSingleInfo(parameter1) {
        var parameterSplit = parameter1.split(",");
		var newObjectName = {}
		newObjectName.firstName = parameterSplit[0];
		newObjectName.lastName = parameterSplit[1];
		newObjectName.email = parameterSplit[2];
		newObjectName.time = new Date(parameterSplit[3]);
		
		var nameExp = new RegExp("\[^a-z,A-Z]");
		var emailExp = new RegExp("\[@,.]");
		var firstTest = nameExp.test(newObjectName.firstName);
		var lastTest;
		var emailTest;
		var timeTest;
		
		if (firstTest == true){
			alert("The first name is not valid. Please retype. ");
			}
			else {
				lastTest == nameExp.test(newObjectName.lastName);
			}
			if (lastTest == true){
			alert("The last name is not valid. Please retype. ");	
			}
			else {
				emailTest == emailExp.test(newObjectName.email);
			}
			if (emailTest == true){
			alert("This email is invalid. Please retype. ");
			}

      /* Stuck here. Not sure how to proceed. HELP!
          If it does, check to see if the time property of the object is set to before the current date and time.
          If it is, add the object to the the past appointments array.
          If it is not, add the object to the future appointments array.*/

			/*else {
			timeTest = ;
			}
			if (timeTest < true){
			.splice("The time is invalid. Please retype. ");
			}*/
		}
		
		
		function printAppointment (appointment) {
			takeSingleInfo(appointment);
			document.write(
			'You have an appointment with <a href="mailto:' + appointment.email+'">' + appointment.firstName + ' ' + appointment.lastName + '</a>  at '
			 + appointment.time.toTimeString() + '<br/>');
		}
		
		
		</script>
