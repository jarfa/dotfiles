.First = function() {
	cat("Successfully loaded .Rprofile at", date(), "\n")	 
	updatePrompt <- function(...) {options(prompt=format(Sys.time(), "%H:%M:%S> ")); return(TRUE)}
	addTaskCallback(updatePrompt)
}
options(repos=c("http://cran.stat.ucla.edu"))
.startup <- new.env() #I'm creating a new env so that rm(list = ls()) doesn't remove these
assign("hh", 
	function(d, nr=6, nc=NULL){
		stopifnot(class(d) == 'matrix' | class(d) == 'data.frame')
		if(is.null(nc)) nc = nr
		r = min(nr, nrow(d))
		c = min(nc, ncol(d))
		d[1:r, 1:c] 
	}, env=.startup) 
assign("qq", function(save1='no') {base::q(save=save1)} , env=.startup) 
attach(.startup)
