# increaseAudioMax
Ex. Youtube increase max sound 
Copy-Paste in console


var audioCtx = new (window.AudioContext || window.webkitAudioContext)();
var myVideoElement = document.getElementsByTagName("video")[0];
var source = audioCtx.createMediaElementSource(myVideoElement); // create a gain node
var gainNode = audioCtx.createGain();
gainNode.gain.value = 3; // 3 - triple the volume
source.connect(gainNode); // connect the gain node to an output destination
gainNode.connect(audioCtx.destination);
