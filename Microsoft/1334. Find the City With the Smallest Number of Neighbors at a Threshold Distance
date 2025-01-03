class Solution {
public:
    int findTheCity(int n, vector<vector<int>>& edges, int distanceThreshold) {
        vector<vector<int>>dist(n,vector<int>(n,10001)) ; 
        for(int i = 0 ; i < n ; i++){
            dist[i][i] = 0 ;
        }
        for(auto & x : edges){
            dist[x[0]][x[1]] = x[2] ;
            dist[x[1]][x[0]] = x[2] ;
        }
        for(int i = 0 ; i < n ; i++){
            for(int j = 0 ; j < n ; j++){
                for(int k = 0 ; k < n ; k++){
                    dist[j][k] = min(dist[j][k] , dist[j][i] + dist[i][k]) ; 
                }
            }
        }
        int ans = -1, countCity =0, minCity = 10001; 
        for(int i = 0 ; i< n ; i++){
            countCity = 0;
            for(int j = 0 ; j < n ; j++){
                if(dist[i][j] <= distanceThreshold){
                    ++countCity;
                }
            }
            if(countCity <= minCity){
                ans = i ;
                minCity = countCity;
            }
        }
        return ans;
    }
};