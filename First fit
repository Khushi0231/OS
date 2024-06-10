#include<iostream>
using namespace std;

int main() {
    int blockSize[10], processSize[10], blockCount, processCount, allocation[10], i, j;

    cout << "Enter the number of blocks: ";
    cin >> blockCount;
    cout << "Enter the number of processes: ";
    cin >> processCount;

    for(i = 0; i < blockCount; i++) {
        allocation[i] = -1;
    }

    for(i = 0; i < blockCount; i++) {
        cout << "Enter the size of block " << i << ": ";
        cin >> blockSize[i];
    }

    for(i = 0; i < processCount; i++) {
        cout << "Enter the size of process " << i << ": ";
        cin >> processSize[i];

        for(j = 0; j < blockCount; j++) {
            if(blockSize[j] >= processSize[i]) {
                allocation[i] = j;
                blockSize[j] -= processSize[i];
                break;
            }
        }
    }

    cout << "\nProcess no.\tProcess size\tBlock no.\n";
    for(i = 0; i < processCount; i++) {
        cout << i << "\t\t" << processSize[i] << "\t\t";
        if(allocation[i] != -1) {
            cout << allocation[i] << endl;
        } else {
            cout << "Not Allocated" << endl;
        }
    }

    return 0;
}
