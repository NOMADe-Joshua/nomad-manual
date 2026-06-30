# How to upload your data

The first thing and what most often leads to problems: You define your experiments with an Excel table, which creates the unique IDs for your substrate and the uploaded raw data from measurements need to map them with the same name. (An explanation on how to make the right Excel table can be found in [Excel Creator](Excelcreator.md)).

--- 

## Right Naming

The goal for everyone is to create an absolute unique ID per substrate. The standard structure looks like: `KIT_NaMe_DateinYYYYMMDD_Batch_Subbatch_Sample`, where `KIT` is always the same, your `NaMe` is made by the first two letters of your first name and surname (Joshua Damm &rarr; JoDa), the `Batch` name and `Subbatch` name can be choosen freely and the `Sample` should be in the best case your Sample name, that is written on your substrate. If you want to map your raw data to your defined samples with unique ID, choose the right ending: 

<table>
  <tr>
    <td>JV</td>
    <td>&rarr;</td>
    <td>jv</td>
  </tr>
  <tr>
    <td>EQE</td>
    <td>&rarr;</td>
    <td>eqe</td>
  </tr>
  <tr>
    <td>MPP</td>
    <td>&rarr;</td>
    <td>mpp</td>
  </tr>
  <tr>
    <td>UVVis</td>
    <td>&rarr;</td>
    <td>uvvis</td>
  </tr>
  <tr>
    <td>PLQY</td>
    <td>&rarr;</td>
    <td>abspl</td>
  </tr>
  <tr>
    <td>SEM</td>
    <td>&rarr;</td>
    <td>sem</td>
  </tr>
</table>

The measurement files can be set together by the `unique ID.measurement.ending`. For example: `KIT_JoDa_20260603_testbatch_1_A1.jv.txt`. Even better is to give the pixel information, if availabe, and the cycle information. They can be given together or just one of them: `unique ID.pxNCycle_M.measurement.ending`, `unique ID.pxN.measurement.ending` or `unique ID.Cycle_M.measurement.ending`, where N and M are natural numbers and M starts at 0 e.g. `KIT_JoDa_20260603_testbatch_1_A1.px1Cycle_0.jv.txt`. If you measure e.g. multiple times PLQY on one sample, the only chance to upload all of them is adding different cycles + you can not add pixel informations. Another extra information can be given with the EQE measurement. As you might have different measurements due to different layers, you can give there the junction information: `bottom`, `middle`, `top`or you do not write anything. See: `unique ID.position.pxNCycle_M.measurement.ending` or `KIT_JoDa_20260603_testbatch_1_A1.bottom.px1Cycle_0.eqe.txt`. For help with automated renaming, see [Data Tools](Datatools.md).

!!! info "Tip to not waste too much of your lifetime"
    If you measure your samples, give them the right ELN name (**unique ID**) from the begin with at the measurement setup and do not run 5 scripts to rename them or even rename them by hand!

---

## Where to upload your files?

--- 

Go as in the video shown to: `Publish` &rarr; `Uploads`and click on `Create a new Upload`. In the picture below you can see the important buttons for you in red. You can give your upload a name, share it with people or groups, reprocess the upload and upload your files. **The black rectangle and everything below is for publishing data global, what you don´t want in the beginning**. 

<video autoplay muted loop playsinline preload="auto" src="/assets/images/first-upload.mp4" 
       class="md-shadow" 
       style="width: 100%; max-width: 1100px; border-radius: 8px; overflow: hidden;">
</video>

Please share your data with people. By clicking on group instead of user, you can search for `pero`and find a few groups: all, nextGen, tandem, printCoat, vapor and test. Please share your data in all, so everyone can see them. If you don´t want to share them with everyone, share them at least for your subgroup (nextGen &rarr; Ulis subgoup, vapor &rarr; Pauls subgroup, tandem &rarr; Renjuns subgroup, printCoat &rarr; currently also Ulis subgroup). If your uploaded data, don`t show SUCCESS, but FAILURE, click on reprocess. If it doesn´t work the second time, ask somebody for help.

<div class="md-shadow" style="width: 100%; max-width: 1100px; border-radius: 8px; overflow: hidden; cursor: zoom-in;">
  <img src="/assets/images/first-upload.png" 
       loading = "eager"
       style="width: 100%; display: block; transition: transform 0.1s ease-out;"
       onmousemove="
         const rect = this.getBoundingClientRect();
         const x = ((e = window.event || arguments[0]).clientX - rect.left) / rect.width * 100;
         const y = (e.clientY - rect.top) / rect.height * 100;
         this.style.transformOrigin = `${x}% ${y}%`;
         this.style.transform = 'scale(1.8)';
       "
       onmouseleave="
         this.style.transform = 'scale(1)';
       ">
</div>

## Access your data

Please check first, that your data were upload correctly with the [Batch Overview](Batchoverview.md) script and access your data then with the different Voilá script like [JV Voilá](JV.md).