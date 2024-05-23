Input and forcing datasets to recreate the model runs leading to the results in Hamm et al. 2024: 
Model-based analysis of solute transport and potential carbon mineralization in a permafrost catchment under seasonal variability and climate change

The simulations were performed using ATS v1.4

Guide:
[] data
  * contains the mesh (.exo) used to perform the spinup and transient simulations
  * contains the forcing data (.h5), which includes the weather data extracted from the adventdalen and LYR airport weather stations
  * contains the column_data.h5 and freezeup_checkpoint_final.h5 file, which is needed as initial condition to perform the spinup
[] input_files
  * 00_freezeup.xml: first spinup step
  * 01_permafrost_column.xml: second spinup step
  * 02_spinup_real_rain.xml: third spinup step ("real_rain" refers to the distribution of precipitation according to the probability density of precipitation events in the weather data)
  * 03_production.xml: production run, which is a continuation of the spinup, but with added transport capabilities and the injection of a tracer. This yields the results for the seasonal active layer transport velocities
  * 05_3abrupt_warming.xml: abrupt warming scenario with a 3°C increase in air temperatures
  * 05_5abrupt_warming.xml: abrupt warming scenario with a 5°C increase in air temperatures
  * 05_transient_rcp45.xml: gradual warming scenario according to an increase of air temperature in line with the RCP 4.5 scenario
  * 05_transient_rcp85.xml: gradual warming scenario according to an increase of air temperature in line with the RCP 8.5 scenario
