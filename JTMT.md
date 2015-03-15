# Introduction #

Clustering works on the term-document matrix.
DocumentCollection wrapper exists to hold the td matrix.
```
class DocumentCollection {
    private RealMatrix tdMatrix;
    private Map<String,RealMatrix> documentMap;
    private List<String> documentNames;

    vectorGenerator.generateVector(documents);
    IdfIndexer indexer = new IdfIndexer();
    tdMatrix = indexer.transform(vectorGenerator.getMatrix());
    documentNames = vectorGenerator.getDocumentNames();
    documentCollection = new DocumentCollection(tdMatrix, documentNames);  
  
    List<Cluster> clusters = clusterer.cluster(documentCollection); }}}
```

Bag of words for individual documents.
Bag of words for the whole collection. (combining individual bag of words removing repetitions.)

Inverted File Structure.
```
net.sf.jtmt.clustering.DocumentCollection
net.sf.jtmt.clustering.ClusteringTest
net.sf.jtmt.indexers.VectorGenerator
net.sf.jtmt.indexers.IdfIndexer
```