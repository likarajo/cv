<div align="center">
  <img alt="Logo" src="logo.png" width="100" />
</div>

My **Curriculum Vitae** built with the [pagedown package](https://pagedown.rbind.io). 

### The main files

- `index.Rmd`: Source template for the CV, contains a variable `PDF_EXPORT` in the header that is used to changes styles for the pdf and html formats. 
- `index.html`: The final output of the CV template when the header variable `PDF_EXPORT` is set to `FALSE`. View it at [likarajo.github.io/cv](http://likarajo.github.io/cv).
- `rajarshi_cv.pdf`: The PDF version of the online CV when it is printed as PDF. Links are put in footer and link to the online version is specified in the sidebar.
- `resume.Rmd`: Source template for a single page resume. 
- `resume.html`: The final output of the resume template when the header variable `PDF_EXPORT` is set to `FALSE`. View it at [likarajo.github.io/cv/resume.html](http://likarajo.github.io/cv/resume.html). 
- `rajarshi_resume.pdf`: The PDF version of the online resume when it is printed as PDF.
- `my_data.csv`: A csv with columns containing the various fields needed for an entry in the CV. A column `section` is used to identify the different entries of projects, jobs, blogs, education, etc.
- `css/`: Directory containing the custom CSS files used to tweak the default 'resume' format from _pagedown_. 

### Open Source usage

1. Fork this repo to your machine with RStudio.
2. Customize the `index.Rmd` for CV and `resume.Rmd` for resume.
3. Edit the rows of `my_data.csv` with your own data.
4. Print each unique `section` (as encoded in the `section` column of `my_data.csv`) in your `.Rmd` with the command `my_data %>% print_section('section_name')`.
5. Knit to html using
6. Print the html as pdf using Chrome browse.