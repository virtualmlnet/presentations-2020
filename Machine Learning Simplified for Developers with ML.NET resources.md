# Additional resources for Machine Learning Simplified for Developers with ML.NET talk

## Code from scratch similar to Model Builder demo

https://jkdev.me/simple-machine-learning-classification/

It's a bit old code but if you're interested in how to build bank transaction classifier from scratch in [ML.NET](https://dotnet.microsoft.com/apps/machinelearning-ai/ml-dotnet), this code might help. It comes with a fined tuned training set in JSON with no evaluation set. (testing is done in unit tests instead)

In the repo you can see:
* How to manually configure training pipeline
* How to use AutoML (and how it's different from above)
* Sample console app with 2 training modes (manual setup and AutoML)
* Sample Blazor server side app
    * On-the-fly [ML.NET](https://dotnet.microsoft.com/apps/machinelearning-ai/ml-dotnet) model in the dependency injection generated once
    * Instructions which part of [ML.NET](https://dotnet.microsoft.com/apps/machinelearning-ai/ml-dotnet) can be singleton and which one shouldn't be with links to official documentation
    * An exampl of determining category labels from the score array we get when we predict a classification

![Cmd Dotnet Run](https://github.com/jernejk/MLSample.SimpleTransactionTagging/raw/master/assets/cmd-dotnet-run.png)
**Figure: Run Console application with training.**

![Cmd Dotnet Run No Training](https://github.com/jernejk/MLSample.SimpleTransactionTagging/raw/master/assets/cmd-dotnet-run-no-training.png)
**Figure: Run Console application without training.**

![Cmd Dotnet Run Auto Ml](https://github.com/jernejk/MLSample.SimpleTransactionTagging/raw/master/assets/cmd-dotnet-run-auto-ml.png)
**Figure: Running AutoML in console application.**

![Blazor Uber Sample](https://github.com/jernejk/MLSample.SimpleTransactionTagging/raw/master/assets/blazor-uber-sample.png)
**Figure: Example of Blazor application.**

![Automl Blazor Training](https://github.com/jernejk/MLSample.SimpleTransactionTagging/raw/master/assets/automl-blazor-training.gif)
**Figure: Running AutoML in Blazor application.**

GitHub: https://github.com/jernejk/MLSample.SimpleTransactionTagging

**PS:** Training data is in JSON, so you won't be able to use this in Model Builder directly. Also, the training data has no duplicates which means that default 50:50 split for training/evaluation will result in a terrible model.

## AutoML generator

https://jernejk.github.io/AutoML.CodeGenerator/

If you prefer to write [ML.NET](https://dotnet.microsoft.com/apps/machinelearning-ai/ml-dotnet) AutoML but don't want to write all of the code, I have made a prototype in Blazor WASM app, where you can enter CSV headers and than select what type of columns they are.

This will then generate a code you can paste in your program.

![Automl Blazor Training](https://github.com/jernejk/AutoML.CodeGenerator/raw/master/assets/csv-headers-with-column-definitions.png)
**Figure: Define CSV headers and specify what kind of column they are.**

![Automl Blazor Training](https://github.com/jernejk/AutoML.CodeGenerator/raw/master/assets/generated-automl-method-code.png)
**Figure: Generated ML.NET AutoML code that you copy/paste in your project!**

GitHub: https://github.com/jernejk/AutoML.CodeGenerator