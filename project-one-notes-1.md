# project one (llvm project) draft 1

## c++ program code ideas: 

  - a simple program with a graph algorithm
  - begins with a list of four Strings which is the input sentence
  - then it creates a graph with each of those words as a node
  - next: apply a transformer algo with a python package and produce an output string
  - next: break down this code block by block or line by line to understand the IR

```cpp
#include <iostream>
#include <vector>
#include <string>
#include <unordered_map>
#include <unordered_set>

using namespace std;

class Graph {
private:
    unordered_map<string, vector<string>> adjacencyList;

public:
    void addEdge(const string& u, const string& v) {
        adjacencyList[u].push_back(v);
        adjacencyList[v].push_back(u); // Assuming undirected graph
    }

    void display() {
        for (const auto& pair : adjacencyList) {
            cout << pair.first << " -> ";
            for (const string& neighbor : pair.second) {
                cout << neighbor << " ";
            }
            cout << endl;
        }
    }
};

int main() {
    vector<string> input = {"This", "is", "a", "sentence"};
    
    Graph graph;
    
    // Create nodes for each word
    for (const string& word : input) {
        graph.addEdge(word, ""); // Adding node for the word
    }
    
    cout << "Graph created with nodes:\n";
    graph.display();
    
    return 0;
}

``
