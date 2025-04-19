# Clustering

## Comparative Performance Study of Clustering Algorithms with Different Preprocessing Techniques
<h3>Dataset:</h3> <br>
Name: Iris Dataset <br>
Size: 150 samples, 4 features <br>
Classes: 3 (Setosa, Versicolour, Virginica) <br>
Type: Multiclass, Numeric <br>

<h3Clustering Algorithms Used:</h3> <br>
<ul><li> K-Means Clustering</li> 

<li>Agglomerative (Hierarchical) Clustering </li>

<li> MeanShift Clustering </li> </ul>

<h3>Preprocessing Techniques:</h3><br>
<ul> <li>No Preprocessing </li>

<li>Normalization (MinMaxScaler)</li>

<li> Transformation (log1p)</li>

<li>  PCA (2D) </li>
<li>Combination:</li>
<ul> <li> Transformation + Normalization </li>
  <li>Transformation + Normalization + PCA </li>
</ul>
</ul>

 <h3> Results </h3>
 <h2>Selected Results:</h2>
    <table>
        <thead>
            <tr>
                <th>Algorithm</th>
                <th>Preprocessing</th>
                <th>Clusters</th>
                <th>Silhouette</th>
                <th>Calinski</th>
                <th>Davies</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>KMeans</td>
                <td>none</td>
                <td>3</td>
                <td>0.551</td>
                <td>561.594</td>
                <td>0.666</td>
            </tr>
            <tr>
                <td>KMeans</td>
                <td>pca</td>
                <td>3</td>
                <td>0.598</td>
                <td>693.708</td>
                <td>0.565</td>
            </tr>
            <tr>
                <td>Hierarchical</td>
                <td>none</td>
                <td>3</td>
                <td>0.554</td>
                <td>558.058</td>
                <td>0.656</td>
            </tr>
            <tr>
                <td>Hierarchical</td>
                <td>pca</td>
                <td>3</td>
                <td>0.598</td>
                <td>688.618</td>
                <td>0.560</td>
            </tr>
        </tbody>
    </table>

    
        Note: Full results with c = 3, 4, 5 for KMeans and Agglomerative Clustering are provided in the notebook.
  
 

<h3>Observations:</h3>
        <ol>
            <li>MeanShift with transform preprocessing yields the best silhouette score.</li>
            <li>Kmeans with PCA preprocessing yields the best silhouette score for 3 clusters.</li>
        </ol>


