# datos-hidrologicos

## A continuación se llevará a cabo un analisis sobre dos cuencas hidrograficas llamadas Estrella y Banano 

inp <- read.csv("FDC.csv", na.strings="")

head(inp)

dim(inp)

inp[!complete.cases(inp),]

# newinp <- na.omit(inp)

plot(inp[,2],type = "l",col="blue")
lines(inp[,3], col="green")

summary(inp[,2:3])
hist(inp[,2])
hist(inp[,3])

names(inp) <- c("fecha","Estrella", "Banano")
attach(inp)
      
plot(Estrella)