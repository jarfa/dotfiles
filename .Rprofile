.First = function() {
	cat("Successfully loaded .Rprofile at", date(), "\n")	 
	updatePrompt <- function(...) {options(prompt=format(Sys.time(), "%H:%M:%S> ")); return(TRUE)}
	addTaskCallback(updatePrompt)
}
options(repos=c("http://cran.stat.ucla.edu"))
.startup <- new.env() #I'm creting a new env so that rm(list = ls()) doesn't remove these
assign("hh", 
	function(d, n=5){
		stopifnot(class(d) == 'matrix' | class(d) == 'data.frame')
		r = min(n, nrow(d))
		c = min(n, ncol(d))
		d[1:r, 1:c] 
	}, env=.startup) 
assign("qq", function(save1='no') {base::q(save=save1)} , env=.startup) 
attach(.startup)
