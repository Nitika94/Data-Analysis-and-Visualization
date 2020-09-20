
library(ggplot2)

SmartPhoneData <- read.csv(file.choose()) # Data extracted from https://www.kaggle.com/grikomsn/amazon-cell-phones-reviews?select=20191226-items.csv

PhoneRatings <- ggplot(SmartPhoneData, aes(x=brand, y=rating, fill = brand)) # Basic plot to initialize the x and y axis, with colour fill aesthetics

PhoneRatings <- PhoneRatings +geom_violin(trim = FALSE, width = 1.2) # Violin graph to represent the data distribution according to the aesthetics

PhoneRatings <- PhoneRatings + geom_boxplot(alpha=1.5, width = 0.3, size = 0.8, outlier.color = "red", outlier.shape ="plus", outlier.size = 3, outlier.alpha = 4)+
  geom_jitter(alpha=0.75,color="blue",size = 0.5) # Boxplot with data points represented in Blue and outliers represented in Red.

PhoneRatings <- PhoneRatings + scale_fill_brewer(palette="Pastel1")+ scale_y_discrete(limits=c("1", "2", "3", "4", "5")) + 
  labs(x = "Smartphone Brands", y = "User Rating", title = "Amazon User Ratings for Top 7 Smartphone Brands in 2019", fill = "Brand") + 
  coord_flip() # Design fill colours and required labels

PhoneRatings <- PhoneRatings + theme( plot.title = element_text(color="Black", size=18, face="bold", margin = margin(20,0,20,0),hjust = 0.5), 
                axis.title.x = element_text(color="Black", size=16),
                axis.title.y = element_text(color="Black", size=16),
                axis.text.x = element_text(size=14),
                axis.text.y = element_text(size=14),
                panel.background = element_rect(fill = "grey90"),
                plot.margin = unit(c(0.75,0.75,0.75,0.75), "cm"),
                plot.background = element_rect(fill = "grey99", colour = "black",size = 1),
                panel.grid.major = element_line(size = 0.5, linetype = 'solid',colour = "white"), 
                panel.grid.minor = element_line(size = 0.3, linetype = 'solid',colour = "white"),
                legend.margin = margin(0.5,0.5,0.5,0.5,"cm"),
                legend.key.size = unit(1,"cm"),
                legend.title	= element_text(color="Black", size=12),
                legend.text	= element_text(color="Black", size=10)
) # Using theme function to format the labels

PhoneRatings + pdf(file = "D:/Sem4/InformationVisualization/Assignment1.pdf",width=12,height=10,paper='special')

dev.off()
