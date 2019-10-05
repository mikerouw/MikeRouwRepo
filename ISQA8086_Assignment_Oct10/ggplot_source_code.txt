ggplot(data=site_phenometrics_data_wo_zero_oberservations) +
geom_point(mapping=aes(x=Mean_First_Yes_DOY,y=Phenophase_ID))
ggplot(data=site_phenometrics_data_wo_zero_oberservations) +
geom_point(mapping=aes(x=Mean_First_Yes_DOY,y=Species_ID))
ggplot(data=site_phenometrics_data_wo_zero_oberservations) +
geom_point(mapping=aes(x=Mean_First_Yes_DOY,y=Phenophase_ID,color=Kingdom))
ggplot(data=site_phenometrics_data_wo_zero_oberservations) +
geom_point(mapping=aes(x=Mean_First_Yes_DOY,y=Phenophase_ID),color="blue") +
geom_smooth(mapping=aes(x=Mean_First_Yes_DOY,y=Phenophase_ID),color="black")
ggplot(data=site_phenometrics_data_wo_zero_oberservations) +
geom_point(mapping=aes(x=Mean_First_Yes_DOY,y=Phenophase_ID),color="blue") +
facet_wrap(~ Site_ID, nrow = 2)
ggplot(data=site_phenometrics_data_wo_zero_oberservations) +
geom_bar(mapping=aes(x=Site_Name),color="red")
