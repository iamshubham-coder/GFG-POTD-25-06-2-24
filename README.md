# GFG-POTD-25-06-2-24
You are given an integer k and matrix mat. Rotate the elements of the given matrix to the left k times and return the resulting matrix.


# CODEOFTHEPROBLEM

class Solution {
  public:
    vector<vector<int>> rotateMatrix(int k, vector<vector<int>> mat) {
    int row=mat.size();
   int col= mat[0].size();
   vector<vector<int>> result(row, vector<int>(col, 0)) ;
      k=k%col;
   if(k==0) 
   return mat;
   for(int i=0;i<row;i++){
       int z=0;
       for(int j=k;j<col;j++){
           result[i][z++]=mat[i][j];
           
       }
       for(int j=0;j<k;j++){
           result[i][z++]=mat[i][j];
       }
   }
   return result;
    }
};
