# Stability-Analysis-using-Bode-Plot
## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=1/(S(1+0.5S)(1+0.1S)) using bode plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:
![2](https://github.com/user-attachments/assets/bac625f5-2390-4cb4-babc-27987aa904a4)
![1](https://github.com/user-attachments/assets/69b1dc8a-c13f-40ee-ae6b-5421a643105e)






## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.

## Program: 
```
num=[1];
den=[0.05 0.6 1 0];
sys=tf(num,den)
bode(sys)
grid on;
[gm pm wpc wgc]=margin(sys)
gmindb=20*log10(gm)
if(wpc>wgc)
    disp('stable')
elseif(wpc==wgc)
    disp('marginally stable')
else
    disp('unstable')
end
```


## Output:
<img width="1920" height="1080" alt="CS EXP5" src="https://github.com/user-attachments/assets/a0f60270-4bf9-4fe6-8ea9-1d6efffa2fb2" />

## Result:
Thus the bode plot for the given transfer function was drawn and verified using MATLAB. <br>
Gain margin = 40db <br>
Phase Margin =  70 degree<br>
Gain crossover frequency = 1 rad/sec<br>
Phase crossover frequency = 20 rad/sec<br>
The system is  ------------
