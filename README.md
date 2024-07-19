### https://inuman.github.io/

Json Resume Site ([https://jsonresume.org/](https://jsonresume.org/))

## Complete steps to generate a PDF Resume for JSON Resume along with Custom Themes

This guide details how to generate a well-formatted PDF resume using JsonResume and a custom theme (Kendall in this example) while avoiding theme formatting issues.

**Prerequisites:**

* Make resume first using gist editor or any editor of your choice then copy paste json to gist public and publish*
  
**Steps:**
 Install Node.js first ([https://nodejs.org/en/download](https://nodejs.org/en/download))

1. **Install resume CLI following documentation:**

   ```bash
   npm install -g resume-cli
   ```

2. **Now you’ll be facing theme install issues locally I personally recommend this blog as it work for me it installs theme to current working directory:**

   - https://bhdouglass.com/blog/how-to-build-a-developer-json-resume/

3. **Just type the information it demands in cmd/shell as they are optional:**

4. **After this check your working directory in my case in Terminal it’s:**
   
   - convo@Numans-MacBook-Pro ~ %
   - convo - > this is my working directory
   - on window it can be you user name folder
   - There’ll be a folder created with name **node_modules** your NodeJs project now setup along with your installed theme and theme will be available now **location : convo/node_modules/your-theme**

6. **Initialize resume.json using command:**

   ```bash
   resume init
   ```
   - t’ll now create resume.json file in working directory now copy your information from resume.json file you created earlier to it.I recommend don’t just replace whole json instead leave the initialised parts in newly created resume.json as it is.
    
7. **Copy Your JsonResume Data that you've created:**
   - Replace the placeholder content in `resume.json` with your actual JsonResume data.
   - **Important:** Retain the initial structure provided by `resume init`.

8. **Now here comes the issue if we use command with specific theme or no theme directly:**
   ```bash
     resume export resume.pdf --theme=kendall
     ```
   - our pdf will be generated in same directory but theme will get disturb it was Kendall in my case
   - To solve this issue

8. **Export Resume in HTML Format first:**

   ```bash
   resume export resume.html --theme=kendall
   ```

   This generates an HTML file named `resume.html` in your project directory, styled using the Kendall theme.

9. **Convert HTML to PDF:**

   - Use an online HTML-to-PDF converter like Sejda ([https://www.sejda.com/](https://www.sejda.com/)).
   - Upload `resume.html` to the converter.
   - Download the generated PDF.

**Congratulations!** You now have a well-formatted PDF resume using your custom theme.
