##Programming Assignment2: Caching the Inverse of a Matrix

In this assignment our task is to write a pair of functions that calculates and caches the inverse of a matrix. For this assignment, we are told to assume that the matrix supplied is always invertible.

<<<<<<< HEAD
In this assignment our task is to write a pair of functions that calculates and caches the inverse of a matrix. For this assignment, we are told to assume that the matrix supplied is always invertible.

The first function called ?makeCacheMatrix? creates a special "matrix" object that can cache its inverse.

makeCacheMatrix <- function(x = matrix()) {
    inv <- NULL
    set <- function(y) {
=======
The first function called ‘makeCacheMatrix’ creates a special "matrix" object that can cache its inverse.

    makeCacheMatrix <- function(x = matrix()) {
        inv <- NULL
        set <- function(y) {
>>>>>>> c0940bc58bc82c659785bc7d2ff47d0c27cf84a3
        x <<- y
        inv <<- NULL
    }
        get <- function() x
        setinverse <- function(inverse) inv <<- inverse
        getinverse <- function() inv
        list(set=set, get=get, setinverse=setinverse, getinverse=getinverse)
}

<<<<<<< HEAD
The second function`cacheSolve`computes the inverse of the special "matrix" returned by `makeCacheMatrix` above. If the inverse has already been calculated (and the matrix has not changed), then `cacheSolve` should retrieve the inverse from the cache.
=======
The second function`cacheSolve`computes the inverse of the special "matrix" returned by `makeCacheMatrix` above. If the inverse has
already been calculated (and the matrix has not changed), then `cacheSolve` should retrieve the inverse from the cache.
>>>>>>> c0940bc58bc82c659785bc7d2ff47d0c27cf84a3


    cacheSolve <- function(x, ...) {
        inv <- x$getinverse()
        if(!is.null(inv)) {
        message("getting cached data.")
        return(inv)
        }
        data <- x$get()
        inv <- solve(data)
        x$setinverse(inv)
        inv
}

