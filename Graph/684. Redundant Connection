/*Understanding this problem begins when you realize that you need to build an adjacency list and use DFS to detect cycles.
If a cycle is detected, return that edge*/
var findRedundantConnection = function(edges) {
    let aL = {};
    for(let [a,b] of edges){
        if(!aL[a]) aL[a] = [];
        if(!aL[b]) aL[b] = [];
        aL[a].push(b);
        aL[b].push(a);
        if(dfs(b,a,a)) return [a,b];
    }
    function dfs(node, target, prev) {
        if(node == target) return true;
        for(let subnode of aL[node]){
            if(subnode != prev && dfs(subnode, target, node)) return true;
        }
        return false;
    }
};
