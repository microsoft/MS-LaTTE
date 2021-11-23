# MS-LaTTE Dataset

The Microsoft Locations and Times of Task Execution (**MS-LaTTE**) dataset is a collection of 10,101 to-do tasks, each of which is annotated for the likely locations and times of day at which it is completed. It is stored in the file **`MS-LaTTE.json`**.

Each to-do task has been annotated by 3 annotators for location and 5 annotators for time to represent the propensities of different people, and resulting diversity, in when and where tasks are most often completed.

In the dataset, each entry is a json dictionary with the following keys:

1. **ID**: an identifier for instances in the data.

2. **TaskTitle**: the name of the to-do task.

3. **ListTitle**: the name of the list in which the to-do task often appears.

4. **LocJudgements**: a list of 3 or 4 judgements for the likely locations at which this to-do task is completed. 4 judgements are supplied in cases when there is a 3-way disagreement between the first 3 judgements. Further, each judgement contains the following properties:

	- **Known**: a boolean value, indicating whether this to-do task is known to the annotator. The location labels specified below are given if and only if the value is Yes.
	- **Locations (optional)**: one or more broad location categories. They can be Home, Work or Public.
	- **PublicLocations (optional)**: one or more fine-grained public location categories, specified when Public is noted as one of the broad **Locations** categories. This list is populated from amongst 69 public location labels.

5. **TimeJudgements**: a list of 5 judgements for the likely times of day at which this to-do task is completed. Each judgement contains the following properties:

	- **Known**: a boolean value, indicating whether this to-do task is known to the annotator. The time labels are given if and only if this value is Yes.
	- **Times (optional)**: one or more times of day. These time labels are combinations of weekday (WD) or weekend (WE), and morning, afternoon, evening, night and anytime, yielding a total of 10 possible time labels.

### Note

As described in our [paper](https://arxiv.org/abs/2111.06902), a pipeline to preserve user privacy was run on the source data to anonymize it. This included a replacement of names and numbers with random alternatives. As a result, there are some task descriptions in the data that may appear strange, such as "0 cucumbers" or "0 nails".

## Citation

If you use the MS-LaTTE dataset in your work, please cite the following:

```
@article{jauhar2021mslatte,
      title={MS-LaTTE: A Dataset of Where and When To-do Tasks are Completed}, 
      author={Jauhar, Sujay Kumar and Chandrasekaran, Nirupama and Gamon, Michael and White, Ryen W.},
      journal={arXiv preprint 2111.06902},
      year={2021}
}
```

## Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## Trademarks

This project may contain trademarks or logos for projects, products, or services. Authorized use of Microsoft 
trademarks or logos is subject to and must follow 
[Microsoft's Trademark & Brand Guidelines](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks/usage/general).
Use of Microsoft trademarks or logos in modified versions of this project must not cause confusion or imply Microsoft sponsorship.
Any use of third-party trademarks or logos are subject to those third-party's policies.
