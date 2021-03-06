# HW - Audio Visualizer - Part I

## I. Overview
In part I of this HW, you will be learning about the HTML5 [WebAudio API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API), and how to utilize it to create an audio visualizer. Topics explored:

1. The [JavaScript IIFE](https://developer.mozilla.org/en-US/docs/Glossary/IIFE) (*Immediately Invoked Function Expression*) pronounced "Iffy" - which is used to keep our variables out of global or "script" scope, and instead make them local to the executed function

2. [Audio Routing Graph](https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API/Basic_concepts_behind_Web_Audio_API#Audio_graphs)

![image](_images/audio-routing-graph.jpg)

3. [AnalyzerNode](https://developer.mozilla.org/en-US/docs/Web/API/AnalyserNode)
  - sampling & bins
  - frequency data - `analyserNode.getByteFrequencyData(data);`
  - waveform data  - `analyserNode.getByteTimeDomainData(data);`
  
4. [JavaScript Typed Arrays](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Typed_arrays) - frequency and waveform data is passed *by reference* to these non-resizable typed arrays.

5. [CORS Restrictions](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS) - ("Cross-origin Resource Sharing") means that you can't run the visualizer start files locally off of your hard drive. You might see an error message like this:

**`MediaElementAudioSource outputs zeroes due to CORS access restrictions for file:///Users/...../soundfile.mp3`**

**Solutions to CORS issues:**
- Run the code off of a web server, which you can do by uploading your code to Banjo
- Use an IDE like [Brackets](http://brackets.io) - which creates a local web server for you to run your code on
- [You can also create a web server using Python](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/set_up_a_local_testing_server) on your local machine
- [Firefox Developer Edition](https://www.mozilla.org/en-US/firefox/developer/) turns off CORS by default, so you don't need a web server

## II. Submission
- the instructions are here: [Audio-Viz-ICE-1.pdf](_files/Audio-Viz-ICE-1.pdf) 
- the start files are zipped up in mycourses
- also see the mycourses.rit.edu dropboxes for due date

## III. One more thing
- this exercise is a few years old, so it declares varibles exclusively with `var`. Go ahead and replace all of the `var` statements with either `let` or `const` as appropriate
