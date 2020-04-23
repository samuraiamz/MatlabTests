# MatlabTests
codes to test my Matlab code
# MatlabA1 
%% set up our motor with initial conditions and properties
% properties
motor.timeConstant = 2/60; % [min]
motor.gain = 0.1;          % [rpm/V]

% transfer function for the motor
s=tf('s');
TFmotor_OL = motor.gain / (motor.timeConstant*s +1);

% plot open-loop response
step(TFmotor_OL, 1)

# script that will test the functions of my code
% test set up our motors with initial conditions and properties
% test motor properties 
motorA.timeConstant = 2/60; % [min]
motorA.gain = 0.1;          % [rpm/V]
motorB.timeConstant = 3/60; % [min]
motorB.gain = 0.3;          % [rpm/V]
motorC.timeConstant = 4/60; % [min]
motorC.gain = 0.4;          % [rpm/V]


%% Test 1: DC brush motorA 
% Test 1 tests if the time.constant and gain of motorA are of appropiate
% value. If it isn't, assert throws an error.
assert(motorA.timeConstant == 2/60); % [min]
assert(motorA.gain == 0.1)          % [rpm/V]

%% Test 2: DC brush motorB
% Test 2 tests if the time.constant and gain of motorB are of appropiate
% value. If it isn't, assert throws an error.
assert(motorB.timeConstant == 2/60); % [min]
assert(motorB.gain == 0.3)          % [rpm/V]
%% Test 3: DC brush motorC
% Test 3 tests if the time.constant and gain of motorC are of appropiate
% value. If it isn't, assert throws an error.
assert(motorC.timeConstant == 2/60); % [min]
assert(motorC.gain == 0.3)          % [rpm/V]
