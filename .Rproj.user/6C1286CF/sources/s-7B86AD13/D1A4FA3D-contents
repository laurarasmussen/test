library(tidyverse)
dat<-read.csv("https://raw.githubusercontent.com/EDUCE-UBC/workshops_data_science/master/reproducible_research/data/data.csv")

dat$Season<-dat$ï..Season

# create plot of oxygen by depth 
O2_plot <- quickplot(data=dat,
                     x=O2_uM,       
                     y=Depth_m,       
                     colour=Season,       
                     main="Saanich Inlet: Seasonal oxygen depth profile")
O2_plot

# save the plot 
ggsave("O2_plot.png")

###Change the axes
O2_plot1 <- quickplot(data=dat,
                     x=O2_uM,       
                     y=Depth_m,       
                     colour=Season,
                     xlab="Oxygen",
                     ylab="Depth profile",
                     main="Saanich Inlet: Seasonal oxygen depth profile")
O2_plot1
# save the plot 
ggsave("O2_plot1.png")

###Color by whether or not microbial data exists for each sample
O2_plot2 <- quickplot(data=dat,
                      x=O2_uM,       
                      y=Depth_m,       
                      colour=Add_data,
                      xlab="Oxygen",
                      ylab="Depth profile",
                      main="Saanich Inlet: Seasonal oxygen depth profile")
O2_plot2
# save the plot 
ggsave("O2_plot2.png")

write.csv(dat, "data.csv")

# read in data 
dat <- read.csv("data.csv")

###Getting info on versions of packages etc
sessionInfo()
