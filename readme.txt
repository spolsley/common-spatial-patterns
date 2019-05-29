Common Spatial Pattern Algorithm for Filter Construction

CSP is a statistical algorithm for construction of spatial filters.  These filters may be used in constructing feature vectors, or other analyses, where it is useful to remove as much noise as possible from a signal.  For example, in a system that classifies between two movements, a given reading will include information from the current task-related activity as well as noise from the other, non-task-related activity.  The classifier will be able to distinguish between the two classes better if a spatial filter is used to reduce noise from the non-task-related activity.

This implementation is a written in python.  To use, simply call CSP(C1,C2,..,Cn) where Cx has the shape (number of samples x feature vector).  That is, each class Cx passed to CSP should be an array where each row is a unique test case/sample.  Each sample will then be a feature vector of some given dimension.  As with other classifiers, the feature vector does not have a required dimension, but it must be the same across all classes in order for the filters to be constructed.

For anyone curious to read more about the algorithm, I based the code on the following paper:

Wang, Yunhua, Patrick Berg, and Michael Scherg. "Common spatial subspace decomposition applied to analysis of brain responses under multiple task conditions: a simulation study." Clinical Neurophysiology 110.4 (1999): 604-614. (available online through Elsevier at https://www.sciencedirect.com/science/article/pii/S138824579800056X)
