% Matlab script based function
% Time constant varied by motors A,B and C. motor.gain constant.
%% set up our motor with initial conditions and properties
% properties
motor.gain = 0.1;          % [rpm/V]

% transfer function for the motor
 s=tf('s');
TFmotor_OL = motor.gain / (motorA.timeConstant*s +1);

% plot open-loop response
step(TFmotor_OL, 1)
