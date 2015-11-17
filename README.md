# SparkDistributedMatrix
This is a research project which aims to provide high performance support for distributed matrix algebra on Apache Spark system. Several distributed matrix format, such as distributed vectors and block partitioned matrices are extensions to the MLlib of Apache Spark machine learning library. For example, several partition schemes are implemented, i.e., MatrixRangePartitioner, MatrixRangeGreedyPartitioner, and BlockCyclicPartitioner.

These partitioners are tailored to provide efficient partitioning over matrix data format. MatrixRangePartitioner simply partitions a matrix based on its rows/cols according to the underlying storage. MatrixRangeGreedyPartitioner makes efforts to achieve the goal that each partition contains approximately the same number of nonzero elements in a greedy way. That means this partitioner does not guarantee exact equal number of  nonzero elements on each partition. For block partitioned matrices, we implemented cyclic partitioner, which adopts block-cyclic distribution strategy for load balancing. 

Specially, we are aiming at enhancing the performance of matrix operation on block matrices. Block partitioned matrices have better data locality property than other types. Also, operations, (e.g, multiplication) can better utilize the sparsity of the input matrices. For more details, please refer to the source code.

### Usage
A typical usage of the library is as follows, 
```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```