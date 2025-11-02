# Radar-Range-Equation-Using-Scilab
## Evaluation of Radar Range Using Scilab

## Aim
To calculate the maximum range of a radar system using the Radar Range Equation and verify the results through Scilab programming.

## Theory 
The Radar Range Equation is a key relationship used in radar system design to determine the maximum distance (range) at which a radar can detect a target.It is given by:

<img width="946" height="468" alt="image" src="https://github.com/user-attachments/assets/3d3dbba8-9df3-4d4d-a231-771426046199" />

## Procedure
1. Refer to the Algorithm and write the Scilab code for the experiment

2. Open Scilab on your system.
   
3. Create a New Editor File: Go to File → New → Script.
   
4. Type Your Code in the editor window.

5. Save the File with a suitable name (e.g., radar_range.sce).

6. Execute the Code: Press F5 or click Execute → File with echo.

7. If Any Errors Occur: Review and correct the code. Save and run it again until it executes successfully.

## Algorithm

1..Initialize constants: λ (wavelength) = 0.03 m σ (radar cross section) = 1 m²

2. Vary each parameter while keeping the others constant: Pt: 0.1 → 10 Gt: 1 → 50 Pm: 1e⁻¹⁵ → 1e⁻¹⁰

3. Compute maximum range using: R_max = ((Pt * Gt² * λ² * σ) / ((4π)³ * Pm))¼

4. Plot the following: Pt vs Rmax Gt vs Rmax Pm vs Rmax

## Program

    lambda = 0.03; 
    sigma = 1;     

    Pt_vals = 0.1:0.1:10;   
    Gt_const = 35;           
    Pm_const = 1e-13;        

    Rmax_Pt = ((Pt_vals .* Gt_const.^2 .* lambda.^2 .* sigma) ./ ((4*%pi)^3 .* Pm_const)).^(1/4);

    Gt_vals = 1:1:50;        
    Pt_const = 2;            
    Pm_const = 1e-13;

    Rmax_Gt = ((Pt_const .* Gt_vals.^2 .* lambda.^2 .* sigma) ./ ((4*%pi)^3 .* Pm_const)).^(1/4);
    Pm_vals = logspace(-15, -10, 50); 
    Pt_const = 2;
    Gt_const = 35;

    Rmax_Pm = ((Pt_const .* Gt_const.^2 .* lambda.^2 .* sigma) ./ ((4*%pi)^3 .* Pm_vals)).^(1/4);   

    subplot(3,1,1);
    plot(Pt_vals, Rmax_Pt, 'b', 'LineWidth', 2);

    subplot(3,1,2);
    plot(Gt_vals, Rmax_Gt, 'r', 'LineWidth', 2);

    subplot(3,1,3);
    plot(Pm_vals, Rmax_Pm, 'g', 'LineWidth', 2);

## Output Waveform
<img width="1919" height="1125" alt="image" src="https://github.com/user-attachments/assets/032ae53f-31ff-4b43-874d-d0512f81022c" />

## Tabulation
![WhatsApp Image 2025-11-02 at 15 33 19_aedeb91b](https://github.com/user-attachments/assets/fc240ced-6e10-414b-bf38-4d7774b15b5f)

## Result
Thus, the maximum range of a radar system using the Radar Range Equation is verified through a Python
program.
