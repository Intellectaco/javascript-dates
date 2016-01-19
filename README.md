# javascript-dates

This repository contains all the functions to manage and manipulate javascript dates, such as getting the time in am and pm format or getting the fullYear.
Hope these functions will help and save time.
<br><br>

#### Check if date is valid
<pre>
function isValidDate(value) {
    var dateWrapper = new Date(value);
    return !isNaN(dateWrapper.getDate());
}
</pre>

#### Compare Number of Days between two dates
<pre>
function compareNumberOfDays(startDate,endDate) {
		return result = startDate.getDay() - endDate.getDay();
}
</pre>

#### Get Full Month Name

<pre>
function getMonthName(today) {
		var monthNames = ["January", "February", "March", "April", "May", "June",
				  "July", "August", "September", "October", "November", "December"
				];
    return monthNames[today.getMonth()]
}
</pre>

#### Compare Time Between two dates
<pre>
function compareTimeBetweenTwoDates(date1, date2) {
	var timediff = (date1.getTime() - date2.getTime()) / 1000; // time in seconds
  return timediff / 60 // time in minutes
}
</pre>

#### Time in AM/PM Format
<pre>
function formatAMPM(date) {
  var hours = date.getHours();
  var minutes = date.getMinutes();
  var ampm = hours >= 12 ? 'pm' : 'am';
  hours = hours % 12;
  hours = hours ? hours : 12; // the hour '0' should be '12'
  minutes = minutes < 10 ? '0'+minutes : minutes;
  var strTime = hours + ':' + minutes + ' ' + ampm;
  return strTime;
}
</pre>
