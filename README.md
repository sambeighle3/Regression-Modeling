# Bootstrapping Regression Statistics

This assignment asks you to use the bootstrap technique we've discussed
to generate bootstrap statistics and compare those to the standard estimates
from R. The details are in `reg_boot.rmd`. Cheers!

When you submit your work, make sure to "knit" your RMD to an `.html` file and include that file in the repo you submit. (You can also knit to PDF and Word formats, which are great, but the HTML files are a bit easier for me to evaluate.) 


## Feedback 

Your opener is good, but you make a mistake on the interpretation of the 
sex variable. With categorical variables the way to assess significance is to
call `anova` on the model object and look at the significance there. I'll 
cover this lecture to make sure it's clear. 

I'd _strongly_ recommend keeping all your variables lowercase (`se_Intercept` vs `se_neither`) and using just underscores (or dots, but I think underscores are more modern now). 

You call these columns "se_", but they're actual values, not standard errors. E.g., your "se_residual" is a collection of actual residual values. 

Be much more specific in you write-up. Talk about the CIs on the coefficients from the bootstrap (with specific numbers) and compare them to the values from `summary.lm`
