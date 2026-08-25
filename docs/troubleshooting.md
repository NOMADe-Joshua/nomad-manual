# Trouble Shooting your Problems

Here you can find standard problems and their solution

---

## What to do, if your upload (e.g. Excel upload) does not show `SUCCESS`, but `FAILURE`?

In the image below, you can see that the Excel table upload wasn´t successful. The `FAILURE`is marked with red.

<div class="md-shadow" style="width: 100%; max-width: 1100px; border: 1px solid black; border-radius: 8px; overflow: hidden; cursor: zoom-in;">
  <img src="../assets/images/FAILURE_bsp.png" 
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

You can check, whats going wrong with clicking on the arrow right to the `FAILURE` and then `LOGS`. The first drop down button will show you the error. See it in the video below:

<video autoplay muted loop playsinline preload="auto" 
       src="../assets/images/troubleshooting_FAILURE.mp4" 
       class="md-shadow" 
       style="width: 100%; max-width: 1100px; border-radius: 8px; overflow: hidden; display: block;">
</video>

The error message is not intuitiv to understand, but once you get used to it, it´s easy to find a hint. You can see the two red boxes in the picture below. The first one gives you the hint, that something is wrong with parsing the `peroTF_Cleaning` class. The second box shows you the problem. There is a ValueError, that happens, because the ELN can´t convert a string into a float (text into a number) with the information `900 s`. 

<div class="md-shadow" style="width: 100%; max-width: 1100px; border: 1px solid black; border-radius: 8px; overflow: hidden; cursor: zoom-in;">
  <img src="../assets/images/FAILURE_bsp_loesung.png" 
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

With checking the Excel file again, you can see in the red box, that the Cleaning step for the IPA cleaning contains an error. In the head is written `Time 2 [s]`, that only accepts a number, as the unit is already written in the head line. With changing the column input from `900 s` to `900`, the error is resolved.

<div class="md-shadow" style="width: 100%; max-width: 1100px; border: 1px solid black; border-radius: 8px; overflow: hidden; cursor: zoom-in;">
  <img src="../assets/images/FAILURE_bsp_loesung_excel.png" 
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

---

## What to do, if your upload says `SUCCESS`, but the Voilá script can´t load your data?

In 99% of the cases your uploaded raw data and your unique IDs defined in your Excel are not the same and the ELN can´t map your measurements on the created substrates. Please check the names in your Excel file and of your measurements before asking.