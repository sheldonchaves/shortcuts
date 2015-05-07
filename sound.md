#Sound

####install
sudo apt-get install sox
####mp3
sudo apt-get install sox libsox-fmt-mp3
####commands
	// change speed
	sox input.wav output.wav speed 3.0  
	//sox input.wav output.wav speed factor-value  
#
Combine multiple audio files into a single file:
sox -m file1.wav file2.wav output.wav  

Copy-Paste a part of an audio file into another file:
sox file.wav output.wav trim [start time in seconds] [duration in seconds]  
sox input.wav output.wav trim 90 120  

audio file backward:
sox input.wav output.wav reverse  

Change the sample rate of an audio file: 
sox input.wav -r 8000 output.wav 

Convert mono audio to stereo and vice versa:
sox mono.wav -c 3 stereo.wav  