## About 

Given that modern recruiting relies heavily on Applicant Tracking Systems to parse, index, and categorize candidates data, this resume is a high-density, highly searchable piece made for senior software developers and/or engineers.

I named this template Strata (the Latin plural of stratum, meaning "layers"). I believe a professional identity is not a static list; it is a narrative built from stacked experiences—education, projects, professional history, and personal initiatives. Most resume templates are category-intensive, forcing expertise into rigid, predefined boxes. Strata is built as a flexible foundation, allowing the story of your expertise to define the structure, not the other way around.

<p align="center">
  <img src="General_view1.jpg" width="380" alt="Resume Page 1 Preview">
  <img src="General_view2.jpg" width="382" alt="Resume Page 2 Preview">
</p>

[![Latest resume preview](https://github.com/pialexandraa/strata-tech-resume/actions/workflows/compile_resume.yml/badge.svg)](https://github.com/pialexandraa/strata-tech-resume/actions/workflows/compile_resume.yml)
 
> 🎀 I also added an automated preview for the resume - it is a GitHub Actions CI/CD pipeline that compiles the LaTeX source and generates fresh PNG previews on every push; it sits in the "assets" dir for now, since I am using the statically-generated images instead.

## Characteristics

* **Single-file implementation:** It is entirely built in LaTeX, in one document, eliminating the hustle of juggling the complex branching logic of various files.
* **Context-driven persona:** This is a dense resume for senior professionals, meaning the resume is context-based and focuses on defining a persona rather than looking at individual, isolated categories (how traditionally we would look at skills, education, experience, etc.).
* **Redefining the Skills category:** The document implements various advanced categories, like publications, and the "Professional Credentials & Modern Stack Exposure"—I thought of this category to work as a display for professional certifications and as a **visual** keyword matching space. This is meant to completely replace the traditional skills section that usually looks like a marginal category, a boring list of items either separated by a comma or listed with bullet points.

<p align="center">
  <img src="keywords_skills_section.jpg" width="700" alt="Resume Category">
</p>

*Mini-disclaimer: ATS-screening tools normally do 2 specific tasks when reading and categorizing a resume:*

*1. Firstly, they take a resume and do a global parsing for keywords; in this case, the Strata template plays fantastically because it is dense in text and specific words.*
*2. Secondly, ATS systems will generally do some sort of categorization, meaning they will look for intuitive category names like "Experience" and "Education" to try to take the information and place it into a specific field of the database when creating the candidate profile. Worst-case scenario, this category information will be distributed to the "Others" category.*

*Finally, a recruiter checks the resume and sees the keywords popping up and the context clearly displayed.*
  
* **Dual optimization:** Moreover, I tried to make the document optimal and clean-looking from both the code and the rendering perspective (design-wise).
* **Machine readability:** The generated PDF is machine-readable and should read nicely on various viewers; it introduces a standardized dictionary into the binary file to force a 1:1 character match.
* **Typography and aesthetics:** It uses a well-known design with strict typography implementations and warm colors. I personally always loved the disruptive elements found in the Awesome-Resume, but give that is it one file and has a custom LaTeX code for alignment, it is easier to edit, operate with, and has simplicity by design.

## Compile / Build resume

### Option 1: locally

I personally prefer and use Unix-based systems for simplicity and a lower system footprint. However, I will list here the tools to locally compile the LaTeX resume file depending on your operating system.

Installing the distribution:
* Ubuntu/Debian: `sudo apt install texlive-latex-base`
* macOS: `brew install --cask basictex`
* Windows: `Install MiKTeX`

Compiling the resume:
Simply navigate to the repository folder where you downloaded the resume file and run:
`pdflatex main.tex`

_As a resume, besides the pdf file, you might get some additional files like main.log, main.aux, or main.out. Most importantly for checking compilation errors and/or warning, would naturally be the main.log file. Check for explicit issues. The ones I am currently seeing are minor font retrieval ones which are quite standard for the current compilation._

### Option 2: in the browser

For a visual representation and zero local installations/setups, I suggest you use Overleaf. It is free and simple, and helps you easily compile your resume, as you do the changes.

1. Create a free account at [Overleaf.com](https://www.overleaf.com/project).
2. Create a New Project and select Upload Project. Alternatively, you can just copy/paste the whole code from main.tex in a new tex file.
3. Upload the files from this repository. Overleaf will automatically detect the LaTeX source and provide an instantaneous PDF preview. If you just downloaded the files from the repository, remember to delete the screenshot and additional files that are not useful for the actual resume (which should be only one document).
