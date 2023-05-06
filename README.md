Download Link: https://assignmentchef.com/product/solved-ee384-lab-10
<br>
<strong>Materials: </strong>

<ul>

 <li>Time Domain P410 radar  MRM RET software</li>

 <li>USB 2.0 A to Micro-B cable.</li>

 <li>Targets</li>

 <li>Tape measure</li>

</ul>

<strong>Introduction: </strong>

In this laboratory we will explore the effects of coherent integration.  The P410 units transmit very short duration pulses.  The FCC restricts the transmit power to be 50 microwatts.  In order to obtain a received signal that can be detected above the noise floor, multiple pulses are transmitted.  The pulses are coherently combined at the receiver, so that the energy in these pulses is summed.  The MRM allows the user to control the number of pulses in the integration.  This number is set in the pulse integration index (PII) in the control tab.  The index is an integer that ranges from 6 to 15.  It represents a power of 2, so that an index of 7 implies that 2<sup>7</sup>=128 pulses are coherently combined to produce a scan.

To improve the detection of a radar target, the signal-to-noise ratio (SNR) must be increased.  This signal-to-noise ratio is a measure of signal power to noise power.  As a ratio of powers the SNR is a unitless measurement.  It is more conveniently expressed in dB which is 10 times the log base 10 of the ratio.

The received signal power will be proportional to the number of pulses integrated, N.  Since increasing the PII by one doubles the number of pulses integrated, the received signal pulse will increase by 2.  Noise is uncorrelated, so that increasing the PII will not increase the noise power.  Thus a PII increase by 1 will double the SNR, or provide an increase in the SNR of 3 dB.  However increasing the pulse integration index will increase the amount of time it takes to perform a scan.  If you are using the radar to detect motion, this extra delay can result in missing target maneuvers.

<strong>Experiment:  </strong>

For this experiment we will determine the change in the SNR as the pulse integration index is increased.

<ol>

 <li>Apply power to the MRM, start MRM RET and connect to the MRM.</li>

 <li>Set the <strong>Transmit Gain</strong> to 0 so that received signals due to close targets are not saturated.</li>

 <li>Set the <strong>Scan Start</strong> time and <strong>Scan Stop</strong> time to the values calculated in Experiment 2. You will have a maximum range of approximately 2 meters.</li>

 <li>Set the pulse integration index to 6. Take a background scan with no target present.  Log the data and note the file name.</li>

 <li>Place a sphere at a distance of approximately 1.5 meters. Take a scan with the target in place and log the data.</li>

 <li>Repeat steps 5 and 6 increasing the integration index each time until you have a set of scans for each integration index from 6 to 15. For each index value, record the time needed to make a scan.  This can be determined by setting the configuration to change the integration index, and then getting the scan time by using the <strong>Get Configuration</strong>.</li>

 <li>In Matlab open the <em>m</em> file and save the file as <em>Experiment4.m</em>

  <ol>

   <li>Change the code so that it will open and save the data from the background scan and each target scan into appropriately named variables<em>.</em></li>

   <li>Form and plot the difference scans for each of the integration values. Discuss the differences in the scans.</li>

   <li>Calculate the SNR for one scan. From the difference scan, select a range of sample values that appear noise like.  For example for the scan below, the samples between the second and third potential targets are noise like, and can be taken for our noise power measurement.</li>

   <li>To calculate the SNR calculate the signal power by taking the maximum signal value for the target, and squaring it. Calculate the noise power by taking the noise samples and calculating the variance of these samples.  This ratio is the SNR.  Express it as a dB value and record this value.</li>

   <li>Repeat for all of the PII values.</li>

   <li>Plot the SNR values versus the PII. Comment on the relationship of the SNR values.</li>

  </ol></li>

</ol>

<strong>Questions: </strong>

<ol>

 <li>How closely did your measurements of signal to noise ratio follow the predicted increase by 3 dB as PII increases by one? How could you improve these results?</li>

 <li>Discuss how the amount of time to take a scan varies with the increase in PII.</li>

</ol>

<strong>Turn in: </strong>

<strong>6, Plots from MRM Plotter for 7b, 7f, Matlab code (commands) for 7d.</strong>





