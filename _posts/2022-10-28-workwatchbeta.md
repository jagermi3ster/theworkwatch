---
title: Work Watch
layout: none
description: Try it out! Version 1.0
permalink: /workwatch
---

<h3>Work Watch</h3>
<p style="margin:10px 100px 10px 100px; text-align:left">The Work Watch is an interactive, customizable stopwatch program which helps you organize your work sessions. Modify break, notification, and task settings with their respective menus.<br><br>We recommend taking 10-minute breaks every 30 minutes (unless your work session is too short or  constrained). We also suggest hiding the timer so that your session's duration doesn't distract you, but still receive time notifications every 20 minutes keep yourself on track. A maximum of five tasks can be added to the list. Click the "Complete Task" button when one is finished. The timer will automatically reset when all tasks have been completed and display a reflection on your work session</p>
<p id="thealarm"><br>Please wait...</p>
<h4><button id="break">Breaks</button>&emsp; <button id="notif">Notifications</button>&emsp;<button id="task">Tasks</button></h4>
<br>
<h5 id="breakinput" style="transform:translate(+235px, -60px)"><label>Break Info<br></label>
<br>Break interval: <input id="bintvinput" style="text-align:left" type="number" min="1" minlength="1" max="999" value="30"> minutes<br><br>Break duration: <input id="bdurinput" style="text-align:left" type="number" min="1" minlength="1" max="999" value="10"> minutes</h5>
<h5 id="notifinput" style="transform:translate(450px, -60px);width:28%"><label>Notification Info<br></label>
<br>Notification interval: <input id="nintvinput" style="text-align:left" type="number" min="1" minlength="1" max="999" value="20"> minutes</h5>
<h5 id="taskinput" style="transform:translate(+700px, -60px);width:23%"><label>Task Info<br></label><br>Task Name: <input id="tnameinput0" style="text-align:left" type="text" minlength="1" value="My Task">
<br>Task Duration: <input id="tdurinput0" style="text-align:left" type="number" min="1" minlength="1" max="999" value="45"> minutes<br><button id="newtask" class="newtask">Add Task to Tasklist</button></h5>
<p><button id="hide" class="hide">
  <!--HIDE BUTTON HERE-->
</button></p>
<div class="stopwatch" id="stopwatch" style="font-size:32px">
    <!-- STOPWATCH HERE -->
    </div>
<button class="btn-start" id="startBtn">Start</button>
<button class="btn-stop" id="stopBtn">Stop</button>
<button class="btn-reset" id="resetBtn">Reset</button>
<br><button class="taskcomplete" id="taskcomplete">Task Complete</button>
<h4 class="notifbox" id="notifbox">
  <!--NOTIF BOX HERE-->
  </h4>
<h4 class="taskbox" id="taskbox">
  <!--TASK BOX HERE-->
</h4>

<style>
    body {
  color: #FFFFFF;
  background: #000000;
  text-align: center;
  font-family: 'OCR A Std', monospace;
}

#break {
  margin: 40px 50px;
  text-align: center;
  color: #DAD6D6;
  background: #9550B2;
  border:solid 1px #C97CEA;
  border-radius:5px;
  padding:10px 20px 10px;
  letter-spacing: 1px;
  cursor:pointer;
}

#notif {
  margin: 40px 50px;
  text-align: center;
  color: #DAD6D6;
  background: #DD6400;
  border:solid 1px #FABF7A;
  border-radius:5px;
  padding:10px 20px 10px;
  letter-spacing: 1px;
  cursor:pointer;
}

#task {
  margin: 40px 50px;
  text-align: center;
  color: #DAD6D6;
  background: #10ACAC;
  border:solid 1px #7AF2F2;
  border-radius:5px;
  padding:10px 20px 10px;
  letter-spacing: 1px;
  cursor:pointer;
}

#newtask {
  margin:10px;
  font-family: 'Arial';
  background: #E5E5E5;
  font-size: 15px;
}

#hide {
  margin: 1px;
  text-align: center;
  color: #DAD6D6;
  background: #000000;
  border:solid 1px #FFFFFF;
  border-radius:5px;
  padding:10px 20px 10px;
  letter-spacing: 1px;
  cursor:pointer;
}

#startBtn {
  margin: 30px 0px 0px 0px;
  text-align: center;
  color: #DAD6D6;
  background: #008000;
  border:solid px #35492C;
  border-radius:5px;
  padding:16px 40px 16px;
  letter-spacing: 2px;
  cursor:pointer;
}

#stopBtn {
  margin: 0px;
  text-align: center;
  color: #DAD6D6;
  background: #B22222;
  border:solid px #590F20;
  border-radius:5px;
  padding:16px 40px 16px;
  letter-spacing: 2px;
  cursor:pointer;
}

#resetBtn {
  margin: 0px;
  text-align: center;
  color: #000000;
  background: #F0FFFF;
  border:solid px #3E383F;
  border-radius:5px;
  padding:16px 35px 17px;
  letter-spacing: 2px;
  cursor:pointer;
}

#taskcomplete {
  margin: 10px;
  text-align: center;
  color: #000000;
  background: #F7FD44;
  border:solid px #3E383F;
  border-radius:5px;
  padding:16px 35px 17px;
  letter-spacing: 2px;
  cursor:pointer;
}

h2
{
  font-size: 50px;
  letter-spacing: 2px;
  margin: 150px 0 0 ;
}

h3
{
  font-size: 40px;
  letter-spacing: 5px; 
  margin: 30px;
  background: #444444;
  border:solid 5px #444444;
  border-radius:50px;
  padding:16px 40px 16px;
  letter-spacing: 2px;
    
}

h4
{
  font-size: 15px;
  letter-spacing: 1px;
  margin: 1px;
  background: #111111;
  border:solid 2px #444444;
  border-radius: 45px;
  padding:1px 1px 1px;
  letter-spacing: 2px;
  text-align: center;
  width: 50%;
  transform: translate(+47.5%);
}

h5 {
  margin: 10px;
  font-size: 16px;
  color: #000001;
  border: solid 2px #7C7C7C;
  padding: 5px 5px 5px;
  background: #FFFFFF;
  width: 25%;
  border-radius: 5px;
  justify-content: center;
  position: absolute;
  display: none;
}

#stopwatch
{
  margin: 10px;
  font-size: 32px;
  color: #FFFFFF;
  background: #000000;
  width: 13%;
  border-radius: 5px;
  justify-content: center;
  transform: translate(+325%, +36%);
}
</style>

<script>
    let output = document.getElementById('stopwatch');
let constant = 0; //Total time var
let ms = 0; //Display time var
let sec = 0;
let min = 0;
let hr = 0;
let running = 0;
let started = 0;
let notifbox = document.getElementById('notifbox'); //notification box
let notiftext = "This will be a timer notification."; //text in notification box (to be updated with timer run)
let breaktext = "This will be a break notification.";
let tasktext = "This will be a task notification.";
let bintvinp = document.getElementById('bintvinput'); //input boxes for variables
let bdurinp = document.getElementById('bdurinput');
let nintvinp = document.getElementById('nintvinput');
let notifintv = 20; //default timer variables
let breakintv = 30;
let breaktrig = (breakintv * 6000) //triggers breaks at certain times
let breakend = (breakintv + 1) * 6000; //ends breaks at certain times
let breakdur = 10;
var temptasktext = ""; //will be overwritten later, here for global scale
var taskbox = document.getElementById('taskbox'); //taskbox element
taskbox.innerHTML = "<br>Your tasks will be displayed here.<br><br>" //taskbox text
var taskname = "My Task"; //default task info
var taskdur = 45;
var tasknlist = []; //empty lists to be filled in for task information
var taskdlist = [];
var currenttask = 0; //represents the currently used task
var taskend = 0;
var taskearly = []; //lists of early/late tasks
var taskovertime = [];
var reflection = ""; //to be filled in for reflection later
notifbox.innerHTML = "<br>" + breaktext + "<br><br>" + notiftext + "<br><br>" + tasktext + "<br><br>"; //default notifbox text
alarmnames = [
    "bandalarm", "beachalarm", "calmingalarm", "celestialalarm", "galaxyalarm", "happyalarm", "marchalarm", "soulfulalarm", "spacealarm", "traditionalalarm"
  ]; //to be called upon later to tell program which to use
var alarmname = "placeholder"; //will be determined by fetch_alarm
let whichalarm = "happyalarm"; //default for alarm in case failure to fetch
function alarm_name() {
  console.log(whichalarm) //creates grammatically correct names for alarms
  if(whichalarm == "bandalarm") {
    var alarmname = "Band Alarm";
  } else if(whichalarm == "beachalarm") {
    var alarmname = "Beach Alarm";
  } else if(whichalarm == "calmingalarm") {
    var alarmname = "Calming Alarm";
  } else if(whichalarm == "celestialalarm") {
    var alarmname = "Celestial Alarm";
  } else if(whichalarm == "galaxyalarm") {
    var alarmname = "Galaxy Alarm";
  } else if(whichalarm == "happyalarm") {
    var alarmname = "Happy Alarm";
  } else if(whichalarm == "marchalarm") {
    var alarmname = "March Alarm";
  } else if(whichalarm == "soulfulalarm") {
    var alarmname = "Soulful Alarm";
  } else if(whichalarm == "spacealarm") {
    var alarmname = "Space Alarm";
  } else if(whichalarm == "traditionalalarm") {
    var alarmname = "Traditional Alarm";
  };
};
var temp = 0; //temporary variable to be used in fetch_alarm
//fetch_alarm fetches from our API and defines the alarm that will be used (copied from table from Jokes API)
function fetch_alarm() {
  temp++
  // keys for joke reactions
  const HAHA = "haha";
  const BOOHOO = "boohoo";
  // prepare fetch urls
  const url = "https://workwatch.nighthawkcodescrums.gq/api/jokes";
  const like_url = url + "/like/";  // haha reaction
  const jeer_url = url + "/jeer/";  // boohoo reaction
  // prepare fetch GET options
  const options = {
    method: 'GET', // *GET, POST, PUT, DELETE, etc.
    mode: 'cors', // no-cors, *cors, same-origin
    cache: 'default', // *default, no-cache, reload, force-cache, only-if-cached
    credentials: 'same-origin', // include, *same-origin, omit
    headers: {
      'Content-Type': 'application/json'
      // 'Content-Type': 'application/x-www-form-urlencoded',
    },
  };
  // prepare fetch PUT options, clones with JS Spread Operator (...)
  const put_options = {...options, method: 'PUT'}; // clones and replaces method
  // fetch the API
  fetch(url, options)
    // response is a RESTful "promise" on any successful fetch
    .then(response => {
      // check for response errors
      if (response.status !== 200) {
          error('GET API response failure: ' + response.status);
          whichalarm = "happyalarm";
          return;
      }
      response.json().then(data => {
          console.log(data);
          var returndata = []; //array to let us make sure the correct one is determined the winner in the console
          //the for loop below checks for the like/dislike value of every alarm and picks the one with the best ratio
          for(i = 0; i < data.length; i++) {
            if (data[i]['id'] == 0) {
                returndata = [(data[i]["haha"] - data[i]["boohoo"]), data[i]['id']]
            }
            alarmdata = data[i]["haha"] - data[i]["boohoo"];
            if (returndata[0] < alarmdata) {
                returndata = [alarmdata, data[i]['id']];
            };
          }; //tests for alarm data
          console.log(returndata);
          console.log(returndata[1]);
          whichalarm = (alarmnames[returndata[1]]);
          console.log(whichalarm);
  })});
}; //duplicate due to prior testing
function alarm_name() {
  console.log(whichalarm)
  if(whichalarm == "bandalarm") {
    var alarmname = "Band Alarm";
  } else if(whichalarm == "beachalarm") {
    var alarmname = "Beach Alarm";
  } else if(whichalarm == "calmingalarm") {
    var alarmname = "Calming Alarm";
  } else if(whichalarm == "celestialalarm") {
    var alarmname = "Celestial Alarm";
  } else if(whichalarm == "galaxyalarm") {
    var alarmname = "Galaxy Alarm";
  } else if(whichalarm == "happyalarm") {
    var alarmname = "Happy Alarm";
  } else if(whichalarm == "marchalarm") {
    var alarmname = "March Alarm";
  } else if(whichalarm == "soulfulalarm") {
    var alarmname = "Soulful Alarm";
  } else if(whichalarm == "spacealarm") {
    var alarmname = "Space Alarm";
  } else if(whichalarm == "traditionalalarm") {
    var alarmname = "Traditional Alarm";
  };
  document.getElementById("thealarm").innerHTML = "The current alarm is the " + alarmname + ".";
};
//setTimeout used to ensure that the fetch is given time to complete before alarm_name() fetches the right data
fetch_alarm();
setTimeout(alarm_name, 3000)
//function to play the alarm at breaks
function play_alarm() {
  var alarm = new Audio('../theworkwatch/sound/' + whichalarm + '.mp3');
  alarm.play();
};
//updates the notification box to feature new updated text variables
function update_notifbox() {
  notifbox.innerHTML = "<br>" + breaktext + "<br><br>" + notiftext + "<br><br>" + tasktext + "<br><br>";
};
//checks whether or not the hour/minute/second count is singular
function singularity_check() {
  if (hr != 1){
    hrtext = " hours";
  } else {
    hrtext = " hour";
  }
  if (min != 1){
    mintext = " minutes";
  } else {
    mintext = " minute";
  };
  if (sec != 1){
    sectext = ' seconds';
  } else {
    sectext = ' second';
  };
};
//run in increments to increase time each centisecond
function timer() {
    constant++;
    ms++;
    if(ms >= 100){
        sec++
        ms = 0
    }
    if(sec === 60){
        min++
        sec = 0
    }
    if(min === 60){
        hr++
        min = 0
    }
    if(constant % (notifintv * 6000) == 0) {
      singularity_check()
      if(hr != 0) {
        notiftext = "The timer has been running for " + hr + hrtext + " and " + min + mintext + ".";
      } else {
        notiftext = "The timer has been running for " + min + mintext + ".";
      };
      update_notifbox();
    };
    if(constant == breaktrig && breaktrig != 0) {
      breaktext = "It's break time! Please take a " + breakdur + "-minute break.";
      taskend = taskend + (breakdur * 6000)
      breakend = (breakdur * 6000) + constant;
      breaktrig = (constant + (6000 * (breakdur + breakintv)))
      console.log(constant, breakend, breakintv)
      update_notifbox();
      play_alarm();
    };
    if(constant == breakend) {
      breaktext = "Break time's over. Get back to work!";
      update_notifbox();
      play_alarm();
    };
    if(constant == taskend && taskend != 0) {
      tasktext = 'You anticipated that "' + tasknlist[currenttask] + '" would be completed by now.';
      taskovertime.push(tasknlist[currenttask]);
      update_notifbox();
    };
    //Doing some string interpolation (CREDIT TO "Dr Goul" on Stack Overflow)
    let seconds = sec < 10 ? `0`+ sec : sec;
    let minute = min < 10 ? `0` + min : min;
    let hour = hr < 10 ? `0` + hr : hr;
    //turning time variables into readable timer
    let time = `${hour}:${minute}:${seconds}`;
    output.innerHTML =time;
  };
function readtime(){
  singularity_check()
  if(hr == 0 && min == 0) {
    timetext = sec + sectext;
    return;
  } else if(hr == 0) {
    timetext = min + mintext + " and " + sec + sectext;
  } else {
    timetext = hr + hrtext + ", " + min + mintext + " and " + sec + sectext;
  }
}
//Starts the timer after checking for variable problems
function start(){
 if (running == 0){
   if(started == 0) {
    breaktext = "This will be a break notification."
    notiftext = "This will be a timer notification."
    tasktext = "This will be a task notification."
    started = 1
    }
   update_notifbox() //code underneath checks if user inputs are valid
   taskend = (taskdlist[0] * 6000);
   if(Math.round(Number(bintvinp.value)) > 0) {
     breakintv = Math.round(Number(bintvinp.value))
     breaktrig = (breakintv * 6000)
   } else {
     breaktext = "Input a break interval as an integer greater than zero."
     update_notifbox()
     return
   };
   if(Math.round(Number(bdurinp.value)) > 0) {
     breakdur = Math.round(Number(bdurinp.value))
   } else {
     breaktext = "Input a break duration as an integer greater than zero."
     update_notifbox()
     return
   };
   if(Math.round(Number(nintvinp.value)) > 0) {
     notifintv = Math.round(Number(nintvinp.value))
   } else {
     notiftext = "Input a notification interval as an integer greater than zero."
     update_notifbox()
     return
   }
   time = setInterval(timer,10)
   //running variable prevents it from being pressed until it's not running
   running = 1
 }
}
//stops the timer
function stop(){
    running = 0;
    try {
      clearInterval(time);
    }
    catch(err) {
      return;
    };
};
//resets the timer and all of the variables, stops the timer
function reset(){
    stop();
    running = 0;
    constant = 0;
    sec = 0;
    min = 0;
    hr = 0;
    output.innerHTML = `00:00:00`
    let notiftext = "This will be a timer notification.";
    let breaktext = "This will be a break notification.";
    let tasktext = "This will be a task notification.";
    update_notifbox();
    tasknlist = [];
    taskdlist = [];
    currenttask = 0;
    console.log(tasknlist, taskdlist)
    taskbox.innerHTML = "<br>Your tasks will be displayed here.<br><br>";
    newtaskBtn.style.background = "#E5E5E5";
    newtaskBtn.innerHTML = "Add Task to Tasklist";
};
//gives a reflection that shows tasks completed late, early
function taskreflect() {
  earlytasks = "Early Tasks: ";
  for(let i = 0; i < taskearly.length; i++) {
    if(taskearly.length == 1) {
      earlytasks = earlytasks + taskearly[i];
    } else {
      earlytasks = earlytasks + taskearly[i]
      if((i + 1) < taskearly.length){
        earlytasks = earlytasks + ", "
      };
    };
  };
  latetasks = "Late Tasks: ";
  for(let i = 0; i < taskovertime.length; i++) {
    if(taskovertime.length == 1) {
      latetasks = latetasks + taskovertime[i];
    } else {
      latetasks = latetasks + taskovertime[i]
      if((i + 1) < taskovertime.length){
        latetasks = latetasks + ", "
      };
    };
  };
};
//function for tc button, sends to the next task
function taskcomplete() {
  if(running == 0){
    return;
  };
  if(constant < taskend) { // If the task is completed before its expected completion time, it's added to a list of early task completions
    taskearly.push(tasknlist[currenttask]);
    console.log(taskearly)
    tasktext = 'You completed "' + tasknlist[currenttask] + '" early. Way to go!';
    update_notifbox();
  };
  currenttask++;
  if(currenttask >= tasknlist.length) {
    readtime();
    reset();
    completiontext = "<br>Congratulations! You completed all of your tasks in " + timetext + ".<br><br>";
    taskreflect();
    if(taskearly.length > 0) {
      completiontext = completiontext + earlytasks + "<br><br>";
    }
    if(taskovertime.length > 0) {
      completiontext = completiontext + latetasks + "<br><br>";
    }
    taskbox.innerHTML = completiontext;
    return;
  };
  taskend = (constant + (taskdlist[currenttask] * 6000));
};
//defining button variables
const startBtn = document.getElementById('startBtn');
const stopBtn =  document.getElementById('stopBtn');
const resetBtn = document.getElementById('resetBtn');
const taskcompleteBtn = document.getElementById('taskcomplete');
//button clicks functions
startBtn.onclick = function() {
  start()
};
stopBtn.onclick = function() {
  stop()
};
resetBtn.onclick = function() {
  reset()
};
taskcompleteBtn.onclick = function() {
  taskcomplete()
};
//editing, giving function for hide timer button
var hidden = 0;
var hw = document.getElementById('hide');
hw.innerHTML = "Hide Time"
var sw = document.getElementById('stopwatch');
hw.onclick = function() {
    if (hidden == 0) {
      sw.style.display = "none"
      hidden = 1
      hw.innerHTML = "Show Time"
    } else {
      sw.style.display = "block"
      hidden = 0
      hw.innerHTML = "Hide Time"
    };
  };
var bihidden = 1; //variables and functions for opening little input windows
var nohidden = 1;
var tahidden = 1;
var breakInp = document.getElementById('breakinput');
var notifInp = document.getElementById('notifinput');
var taskInp = document.getElementById('taskinput');
var newtaskBtn = document.getElementById('newtask');
var breakBtn = document.getElementById('break');
var notifBtn = document.getElementById('notif');
var taskBtn = document.getElementById('task');
notifBtn.onclick = function() {
  if (bihidden == 0) {
    breakInp.style.display = "none"; //makes input windows close other open input windows
    bihidden = 1;
  };
  if (tahidden == 0) {
    taskInp.style.display = "none";
    tahidden = 1;
  };
  if (nohidden == 1){
    notifInp.style.display = "block";
    nohidden = 0;
  } else {
    notifInp.style.display = "none";
    nohidden = 1;
  };
};
breakBtn.onclick = function() {
  if (nohidden == 0) {
    notifInp.style.display = "none";
    nohidden = 1;
  };
  if (tahidden == 0) {
    taskInp.style.display = "none";
    tahidden = 1;
  };
  if (bihidden == 1){
    breakInp.style.display = "block";
    bihidden = 0;
  } else {
    breakInp.style.display = "none";
    bihidden = 1;
  };
};
taskBtn.onclick = function() {
  if (nohidden == 0) {
    notifInp.style.display = "none";
    nohidden = 1;
  };
  if (bihidden == 0) {
    breakInp.style.display = "none";
    bihidden = 1;
  };
  if (tahidden == 1){
    taskInp.style.display = "block";
    tahidden = 0;
  } else {
    taskInp.style.display = "none";
    tahidden = 1;
  };
};
//updates the taskbox
function update_taskbox() {
  temptasktext = ""
  for (let i = 0; i < tasknlist.length; i++) {
  temptasktext = temptasktext + "<br>Task: " + tasknlist[i] + " | Duration: " + taskdlist[i] + " minutes<br>";
  }
  taskbox.innerHTML = temptasktext + "<br>"
}
newtaskBtn.onclick = function() {
  if(tasknlist.length > 4){
    return
  }
  taskname = String(document.getElementById('tnameinput0').value)
  taskdur = Math.round(Number(document.getElementById('tdurinput0').value));
  if(taskname.length > 30){
    return
  }
  if(taskdur < 1 || taskdur > 999) {
    tasktext = "Input a task duration greater than zero minutes and less than 999 minutes."
    update_notifbox()
    return
  }
  tasknlist.push(taskname);
  taskdlist.push(taskdur);
  console.log(tasknlist, taskdlist);
  update_taskbox();
  if(tasknlist.length > 4){
    newtaskBtn.innerHTML = "Maximum Task Number Reached";
    newtaskBtn.style.background = "#747474";
  };
};
</script>