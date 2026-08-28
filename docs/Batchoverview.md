# Batch Overview 

The batch overview script gives you the option to load an upload (your batch) and provide informations over the process steps and your variations.

<div class="md-shadow" style="width: 100%; max-width: 1100px; border: 1px solid black; border-radius: 8px; overflow: hidden; cursor: zoom-in;">
  <img src="../assets/images/OverView_1.png" 
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

It shall answer you the following three questions:

1. **Which processes did you use?**

    You will get a enumaration of your processes you have used.

2. **What did you vary?**

    It does not read your names in the variations column in your excel, but understands what you varied in your excel itself. E.g. if you vary your C60 thickness, it shows you that.

3. **Are there mistakes in your**

    A very common problem in the excel files is, that there can be enumerations errors or that you just forget to add the variation to the distinct process columns. Therefore, it´s super important to check your upload quickly with this script!

In the following picture you can see something unexpected. There are relatable variations and cleaning variations. 

<div class="md-shadow" style="width: 100%; max-width: 1100px; border: 1px solid black; border-radius: 8px; overflow: hidden; cursor: zoom-in;">
  <img src="../assets/images/OverView_2.png" 
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

By clicking on detail, you can see that the user did not write `O2` for the plasma in this example, but enumerated the numer to O3, O4, O5, ... The Batch Overview script helps you to detect most of the common mistakes. 

<div class="md-shadow" style="width: 100%; max-width: 1100px; border: 1px solid black; border-radius: 8px; overflow: hidden; cursor: zoom-in;">
  <img src="../assets/images/OverView_3.png" 
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