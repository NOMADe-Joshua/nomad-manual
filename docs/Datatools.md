# Renaming or splitting files and correct file name endings &rarr; Data Tools

As the software of most of our measurement setups does not work nicely together with the structure of the ELN, the Voila script Data Tools should help you renaming your data, adding the right ending to your file names or split the files (puri). Go to [Voilá](http://elnserver.lti.kit.edu/nomad-oasis/gui/search/voila){ .md-button .md-button--primary .small-button target="_blank" rel="noopener noreferrer"} and start the `Data Tools` script with the :material-open-in-new: button on the right. 

<div class="md-shadow" style="width: 100%; max-width: 1100px; border: 1px solid black; border-radius: 8px; overflow: hidden; cursor: zoom-in;">
  <img src="../assets/images/DataTools_1.png" 
       loading="eager"
       style="width: 100%; display: block; transition: transform 0.1s ease-out;"
       onmousemove="
         const e = window.event || arguments[0] || event;
         const rect = this.getBoundingClientRect();
         const x = (e.clientX - rect.left) / rect.width * 100;
         const y = (e.clientY - rect.top) / rect.height * 100;
         this.style.transformOrigin = x + '% ' + y + '%';
         this.style.transform = 'scale(1.8)';
       "
       onmouseleave="this.style.transform = 'scale(1)';">
</div>

1. **Puri Split**

    1. The script is made to split the puri JV files as each measurement contains every pixel. The script has less functions for the tandem puri setup as there is no request, but the script contains the following features for the tfl setup.

    2. You can upload every generated file with your measurements and it understands what to kick out, what to split and rename and whether you measured MPP. If you measured MPP, it also renames these files and adds the `mpp` file ending.

    3. The split script always adds the cycle information and naturally starts with 0. If you measured multiple cycles in one file, it counts up the cycle. If you have multiple files named the same way, it also counts up the cycle and does not delete measurements. If you measure a sample, it will get the cycle number 0 and if you decide that you want to continue measuring, you can just add `_Cycle_N`, where `N` is 1, 2, 3, ... and it adds it correctly as cycle information to your file name.

2. **JV Rename (Old)**

    Renames the files from the old LabView software in tfl. If you measure multiple cycles there, you can click on the checkbox `Preserve cycle informations in filenames` and it does what it says.

3. **Rename data for ELN integration**

    This script is made to help bring old data with kinda random names into the ELN `KIT_NaMe_DateinYYYYMMDD_Batch_Subbatch_Sample.process.ending` structure. If you give your measurement the right name now, it shouldn´t interest you.

4. **UV-Vis Merger**

    The ELN UVVis integration awaits that you upload your reflection and transmission data within one file. You can use this script to merge the T and R files from the Lambda 1050 and the setup in tfl. The script searches for logic pairs with the same name and for T´s and R´s in the name to check whether it´s a transmission or a reflection file. If you measure your samples, adding `_T` or `_R` to the name will help you here with the automated merge function. You can rename every sample as well pretty easily in this script to bring the name into the ELN name structure.

5. **EQE Splitter**

    If you use the Enlitec system to measure EQE, you can save every measurement in one file and export that one file at the end. This script helps you split it and rename the measurements for the ELN. It lets you choose a position (top, middle, bottom) for multi-junction measurements too :)

6. **Ratio Calculator**

    Lets you calculate weight and molar ratios.