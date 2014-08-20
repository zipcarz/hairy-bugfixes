hairy-bugfixes
==============
var signals = ['cat', 'HIDE CONTENT', 'github'];
var t = Remote.transmitter(signals);

// ideally, signals would be emitted when buttons are clicked
document.querySelector('#cat-button').addEventListener('click', function() {
  t.emit('cat');
});

document.querySelector('#github-button').addEventListener('click', function() {
  t.emit('github');
});

// signals can be emitted any way you like, though
setTimeout(function() {
  t.emit('foo');
}, 5000);
