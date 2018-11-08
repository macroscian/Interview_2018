## Background

We would like you to prepare a presentation, no longer than twenty minutes, on approaches to the following problem. There is no single "right" answer; rather, we're looking to see evidence of deep understanding of your preferred approach.

If you have any difficulties or concerns, please let me know at gavin.kelly@crick.ac.uk. We will post the responses to any questions here, so it may be worth checking it again.

We have provided the data as an R object, but you can analyse the data with tools of your choosing; if you're under time pressure, we don't expect a large body of code or slides, we'd much rather that you consider the issues around such a question, and if you can do that without coding then fine.

## The question

The matrix of data corresponds to the measurement of expression of multiple genes (rows) in many patient samples (columns). The genes are a subset of all human genes, chosen because of their published relevance to a particular clinical status (KRAS activity). The patients all have a cancer in common, but other than that may have different clinical data associated with them, such as survival, stage, grade (none of which are available to us for this study). One thing we do know about them is the result of a pathologist's judging them to be either positive or negative for oncogenic KRAS mutation. This judgement is reasonably reliable.

Different authors have put forward different "signatures" - collections of genes assocated with KRAS activity (which is associated with, but not identical to, oncogenic KRAS mutation), that they have derived from analyses of their own datasets. We have provided a table allowing you to identify which genes appear in which signatures, but the mechanism by which their expression is associated with KRAS activity (strength and direction of effect, etc) is unknown.

We want to know how similar the seven different signatures are in the context of our data: firstly regardless of mutation status; and secondly also taking mutation status of patients into account.

We also have the opportunity to measure the expression of some of these genes in a large number of future patients, in order to infer their KRAS status: how would we go about selecting these, while maintaining as much of the information provided by the signatures as possible.

## The data

[The data](interviewData.rda) is a an R SummarizedExperiment that you can load with `library(SummarizedExperiment);load("interviewData.rda")`. The signatures are accessible via `rowData(interviewData)` and the KRAS mutation status via `colData(interviewData)$mutant`.
