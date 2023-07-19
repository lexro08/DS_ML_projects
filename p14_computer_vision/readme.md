# Determining the age of buyers

The chain supermarket "Bread-Salt" introduces a computer vision system for processing customer photos. Photo fixation in the checkout area will help determine the age of customers in order to:

- Analyze purchases and offer products that may be of interest to buyers of this age group;
- Monitor the integrity of cashiers when selling alcohol.

**Task**
To help the Bread-and-Salt supermarket with the preparation of a model that will determine the age of the buyer from the photo

# Results of the research

The ResNet50 architecture using backbone was taken as the basis for preparing the training model.

The following training parameters were used:
**batch_size=None, epoch=10, steps_per_epoch=None, validation_steps=None,
activation='reg', optimizer=Adam(lr=0,0001), loss='mean_squared_error', metrics=['mean_absolute_error']*

As part of the work carried out to predict the age of the photo, the presented model on the test sample shows the value of MAY 6.2944, which, in turn, is lower than the target metric 8.

**Libraries** - matplotlib, tensorflow
