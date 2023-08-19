class UnionFind {
public: 
    vector<int> parent; 
    UnionFind(int n){
        parent.resize(n);
        for(int i=0;i<n;i++)
            parent[i] = i; 
    }
    
    int findParent(int p) {
        if(parent[p] ==p)return p;

        return  parent[p] = findParent(parent[p]); 
    }
    
    void Union(int u , int v) {
        int pu = findParent(u) , pv = findParent(v); 
        parent[pu] = pv;
    }    
};
