<!--gterm notebook command=r-->
## Graphterm Notebook using R: Example 1


```{r}
# Load GraphTerm API helper functions
source(paste(Sys.getenv("GTERM_DIR"),"/bin/gterm.R", sep=""))

```

```{r}
g <- gcairo()         # Setup Cairo device for GraphTerm
x <- rnorm(100,0,1)
hist(x, col="blue")
g$frame()             # Display plot as inline image
```

```output

format = ARGB (400 x 300)

```

![image][output-fig1-R-example1.R.md]

[output-fig1-R-example1.R.md]: data:image/png;base64,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