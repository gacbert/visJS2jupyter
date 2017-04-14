# visJS2jupyter

visJS2jupyter is a tool to bring the interactivity of networks created with vis.js into jupyter notebook cells, authored by members of the [UCSD Center for Computational Biology & Bioinformatics](http://compbio.ucsd.edu)

## Getting Started

These instructions will get you a copy of the package up and running on your local machine.

### Prerequisites

You must have Jupyter notebook already installed. Visit [here](http://jupyter.org/install.html) for more information.

Install matplotlib before using visJS2jupyter. Visit [here](http://matplotlib.org/users/installing.html) for more information.

To use the visualizations module, install [networkX](https://networkx.github.io/) and [py2cytoscape](https://github.com/idekerlab/py2cytoscape):

```
pip install networkx
pip install py2cytoscape
```

### Installing

visJS2jupyter supports both Python 2.7 and 3.4.

You can install visJS2jupyter using pip:

```
pip install visJS2jupyter
```

In your Jupyter notebook, first import matplotlib:

```
import matplotlib
```

To import visJS_module, use the following:

```
import visJS2jupyter.visJS_module
```

To import visualizations, use the following:

```
import visJS2jupyter.visualizations
```

## Features and Examples
A simple use example is included in the notebooks folder.  In the example provided, we show how to display a graph created with NetworkX using visJS2jupyter.  Here the networks displayed within Jupyter notebook cells may be dragged, clicked, and hovered on, and zooming is enabled within the window.  Nodes and edges may be styled with properties available from vis.js networks (see http://visjs.org/docs/network/ for a list and description of properties).  The main function is 'visjs_network', which requires two inputs which describe the nodes and edges in the network- 'nodes_dict', and edges_dict'.  The other arguments are optional, and apply general styles to the graph, such as sizes, highlight colors, and physics properties of the graph.

An interactive use example of visJS2jupyter may be found [here](http://bl.ocks.org/brinrosenthal/raw/89ef33bebbf2d360099029666b1e8bea/) (scroll to the bottom to see the network).  In this example, we display the bipartite network composed of diseases in [The Cancer Genome Atlas](http://cancergenome.nih.gov/) and the top 25 most common mutations in each disease.  We also overlay information about drugs which target those mutations.  Genes which have a drug targeting them are displayed with a bold black outline.  The user may hover over each gene to get a list of associated drugs.

#### Visualizations
Supplementary module, containing frequently used network visualizations

1) **draw_graph_overlap** takes in two graphs and displays their overlap. Intersecting nodes are triangles and non-intersecting nodes are either circles or squares, depending on which graph they belong to. An interactive example may be found [here](https://bl.ocks.org/julialen/raw/d21c9d378cb09b5a7181497101996727/). In this example, we graph the union of two networks of 10 nodes each. The user can hover over each node to see the graph it belongs to and the node name. 

2) **draw_heat_prop** simulates heat propagation on the network initialized from a given set of seed nodes. It takes in a graph and a list of seed nodes. An interactive example may be found [here](https://bl.ocks.org/julialen/raw/82c316048ade650effbff3fd9eaddccd/). 

3) **draw_colocalization** similarly draws the heat propagation of the graph but with two sets of seed nodes. Another interactive example can be found [here](https://bl.ocks.org/julialen/raw/a82040bdc8b5ba3ca866489db795af74/).

## Authors

* **Brin Rosenthal** (sbrosenthal@ucsd.edu)
* **Julia Len** (jlen@ucsd.edu)
* **Mikayla Webster** (m1webste@ucsd.edu)
* **Aaron Gary** (agary@ucsd.edu)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details