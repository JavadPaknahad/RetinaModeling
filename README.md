The code and methodology presented here describe a computational model aimed at investigating the effects of current waveforms of electrical stimulation of the retina used in prosthetic devices for restoring partial vision lost to retinal degenerative diseases.

Abstract: A computational model of electrical stimulation of the retina is proposed for investigating current waveforms used in prosthetic devices for restoring partial vision lost to retinal degenerative diseases. The model framework combines a connectome-based neural network model characterized by accurate morphological and synaptic properties with an admittance method model of bulk tissue and prosthetic electronics. In this model, the retina was computationally “degenerated,” considering cellular death and anatomical changes that occur early in disease, as well as altered neural behavior that develops throughout the neurodegeneration and is likely interfering with current attempts at restoring vision. A resulting analysis of stimulation range and threshold of ON ganglion cells with the retina that are either healthy or in beginning stages of degeneration is presented for currently used stimulation waveforms, and an asymmetric biphasic current stimulation for subduing spontaneous firing to allow increased control over ganglion cell firing patterns in degenerated retina is proposed. Results show that stimulation thresholds of retinal ganglion cells do not notably vary after beginning stages of retina degeneration. In addition, simulation of proposed asymmetric waveforms showed the ability to enhance the control of ganglion cell firing via electrical stimulation.

AM-NEURON SIMULATIONS

Admittance Method (AM)

Code for the Admittance Method (AM) can be found in folder named "AM".
We provided the resulting output voltages of the AM code after interpolation in the folder named ‘voltage’ and you can simply skip the AM simulations. The resulting voltages of the AM code correspond to the figure 4 in the paper. Details related to the instructions on how to run the AM simulation are also provided in the folder “Instructions on AM”.

NEURON

All NEURON-related code may be found in folder named "NEURON Modeling"

To avoid errors when running the NEURON simulation, make sure to recompile all .mod files before beginning the simulation.

The “morphology” folder includes all the SWC files of the retinal cells modeled in this paper.

In addition to the morphology, the topology of the network was extracted. ‘606celltypes.txt’ and ‘606projections.txt’ files are provided in the directory. These are ASCII text files. The ‘606celltypes.txt’ lists the ID that each cell is given (also used as the filename for the SWC files), and each cell’s cell type. The ‘606projections.txt’ describes every connection within the network (in this case for cell 606 (ganglion cell)), with each line defining a single connection. The fields in each line are defined as:
(source cell ID) (target cell ID) (x-coordinate (source)) (y-coordinate (source)) (z-coordinate (source)) (x-coordinate (target)) (y-coordinate (target)) (z-coordinate (target)) (projection type) (synaptic weight)

The extracellular voltages are computed at each neural compartment for each timestep and saved as .v format. The .v files for reproducing the simulations in the paper are provided inside the NEURON Modleing folder named “voltage”.

After compiling all .mod files load the appropriate .hoc file from the neuron main menu after starting nrngui or by either double clicking in mswin's window explorer, typing nrngui init_SymmetricPulse.hoc in unix, or dragging and dropping the init_SymmetricPulse.hoc file onto the nrngui icon in Mac OS X.

To reproduce Fig. 8 in the paper, simply run “init_SymmetricPulse.hoc” for the symmetric waveform and “init_AsymmetricPulse.hoc” to get the results for the asymmetric waveform.

If you use any part of the code and methodology presented in these pages for your own work, kindly cite:

K. Loizos et al, "Increasing electrical stimulation efficacy in degenerated retina: stimulus waveform design in a multiscale computational model," IEEE Transactions on Neural Systems and Rehabilitation Engineering, vol. 26, no. 6, pp. 1111-1120, 2018.
https://ieeexplore.ieee.org/document/8353348

