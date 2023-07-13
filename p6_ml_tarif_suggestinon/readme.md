# Tariff suggestions

The mobile operator Megaline found out that many customers use archive tariffs. They want to build a system capable of analyzing customer behavior and offering users a new tariff: "Smart" or "Ultra".

We have at our disposal data on the behavior of customers who have already switched to these tariffs (from the course project "Statistical Data Analysis"). We need to build a model for the classification task that will choose the appropriate tariff. 

We need to build a model with the maximum accuracy value. To pass the project successfully, we need to bring the proportion of correct answers to at least 0.75. Check accuracy on the test sample ourself.

# Results of the research

Based on the conducted research, the Decision Tree models with a depth of 3 and a Forest of Trees show themselves best.

The depth of the tree affects the accuracy of predictions. In this case, the greater the depth (up to a certain value) the higher the accuracy.

The accuracy of the Random Forest model reaches 79%.

**Libraries** - 
