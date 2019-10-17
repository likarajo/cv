<div align="center">
  <img alt="Logo" src="logo.png" width="100" />
</div>

My **Curriculum Vitae** built with the [pagedown package](https://pagedown.rbind.io). 

### The main files

- `index.Rmd`: Source template for the cv, contains a variable `PDF_EXPORT` in the header that changes styles for pdf vs html. 
- `index.html`: The final output of the template when the header variable `PDF_EXPORT` is set to `FALSE`. View it at [likarajo.github.io/cv](http://likarajo.github.io/cv).
- `rajarshi_cv.pdf`: The final exported pdf. Links are put in footer and notes about online version are added. 
- `resume.Rmd`: Source template for single page resume. 
- `rajarshi_resume.pdf`: Result for single page resume.
- `my_data.csv`: A csv with columns encoding the various fields needed for an entry in the CV. A column `section` is also available so different sections know which rows to use.
- `css/`: Directory containing the custom CSS files used to tweak the default 'resume' format from pagedown. 

### Open Source usage

1. Fork, clone, download the zip of this repo to your machine with RStudio.
2. Go through and personalize the supplementary text in the Rmd you desire (`index.Rmd` for CV, `resume.Rmd` for resume).
3. Using your spreadsheet editor of choice, replace the rows of `my_data.csv` with your positions.
3. Print each unique `section` (as encoded in the `section` column of `my_data.csv`) in your `.Rmd` with the command `my_data %>% print_section('section_name')`.
