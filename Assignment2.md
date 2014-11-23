makeCacheMatrix<-function(m){
  x<-matrix(rnorm(m*m),m,m)
  xx<-t(x)%*%x
  return(xx)
}

#xx
cacheSolve<-function(xx){
  return(solve(xx))  
}



##########
xx<-makeCacheMatrix(4)
xx
cacheSolve(xx)

cacheSolve(xx)%*%xx
