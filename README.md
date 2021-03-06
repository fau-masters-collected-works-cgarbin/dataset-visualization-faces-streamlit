# Dataset visualization with Facets and Streamlit

Explore dataset visualization with [Google Facets](./google-facets/README.md) and
[Streamlit](./streamlit/README.md).

We use these visualization tools to explore the characteristics of the patients in the
[ChestX-ray8 (a.k.a. ChestX-ray14) dataset](https://arxiv.org/abs/1705.02315) available
[here](https://nihcc.app.box.com/v/ChestXray-NIHCC).

For this analysis we are interested in the characteristics of the patients, not the images. We want
to understand the representativeness of the dataset across genres and ages. We will explore
questions such as:

- What is the overall genre distribution?
- What is the distribution of diseases across the genres?
- What is the distribution of diseases across the ages? Across age groups?
- Is the disease distribution the same in the training and test sets?
- Is the disease distribution the same across genres and ages in the training and test sets?
- What diseases coccur in the same image?

## If you want to explore the visualizations

Clone this repository, then:

### Google Facets visualization quick guide

Note that Google Facets works only with Chrome.

- Google Facets Dive: open Chrome, then choose _Open File..._ in the _File_ and open the file
    `google-facets/google-facets-dive.html`.
- Google Facets Overview: open Chrome, then choose _Open File..._ in the _File_ and open the file
    `google-facets/google-facets-overview.html`.

### Streamlit visualization quick guide

- Set up the environment as explained [here](#if-you-want-to-change-the-code).
- `cd streamlit`
- `streamlit run streamlit-viz.py`

The dataset is fairly large. It may take several seconds to show the page.

## If you want to change the code

These are the quick instructions to work with the code for the visualizations.

- Install Python 3
- Clone this repository
- Go into the repository directory
- Create a Python [environment](https://packaging.python.org/guides/installing-using-pip-and-virtual-environments/#creating-a-virtual-environment):
  `python3 -m venv env`
- Activate the environmnet: `source env/bin/activate` (Linux/Mac) or `.\env\Scripts\activate` (Windows)
- Install the Python packages: `pip install -r requirements.txt`

## Google Facets

See how Google Facets is used to explore the dataset [here](./google-facets).

## Streamlit

See how Streamlit is used to explore the dataset [here](./streamlit).

## Which one should I use?

The fundamental difference between them is that Google Facets does not require any coding.
In fact, you can upload a dataset directly [on their site](https://pair-code.github.io/facets/).
Look for the "load your data" button. Note that, as it says in the button, you are uploading
data to the Google site - think about privacy and intellectual property. (Side note: it is
possible to customize the data points to show an image - this requires some coding, as
explained [here](https://github.com/PAIR-code/facets/blob/master/facets_dive/README.md#providing-sprites-for-dive-to-render),
but it can be used without it).

Not requiring code is an advantage and disadvantage. It is fast to explore the data, as long
as you do not need features beyond what Google Facets already has in place.

Customization is Streamlit's strength. You can transform the data on the fly, add filters and
visualizations not available in Google Facets. The cost is writing the code for that. Streamlit
takes care of the user interface elements and updating the user interface, so you can concentrate
on writing the code that filters the data and creates the visualizations.

To summarize:

- Google Facet is good for a quick inspection of the data.
- Sreamlit is good for customized ways to explore the data.
