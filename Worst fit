#include<iostream>
using namespace std;

int main() {
    int blocksize[10], processsize[10], blockno, processno, flags[10], allocation[10], i, j;

    cout << "Enter the number of blocks: ";
    cin >> blockno;
    cout << "Enter the number of processes: ";
    cin >> processno;

    for(i=0; i<blockno; i++) {
        flags[i] = 0;
        allocation[i] = -1;
    }

    for(i=0; i<processno; i++) {
        cout << "Enter the size of process " << i << ": ";
        cin >> processsize[i];

        int worstFitIndex = -1;
        for(j=0; j<blockno; j++) {
            if(flags[j] == 0 && blocksize[j] >= processsize[i]) {
                if(worstFitIndex == -1 || blocksize[j] > blocksize[worstFitIndex]) {
                    worstFitIndex = j;
                }
            }
        }

        if(worstFitIndex != -1) {
            allocation[worstFitIndex] = i;
            flags[worstFitIndex] = 1;
        }
    }

    cout << "\nBlock no.\tProcess no.\tProcess size\tBlock size\n";
    for(i=0; i<blockno; i++) {
        cout << i << "\t\t";
        if(allocation[i] != -1) {
            cout << allocation[i] << "\t\t" << processsize[allocation[i]] << "\t\t" << blocksize[i] << endl;
        } else {
            cout << "Not Allocated\t" << blocksize[i] << endl;
        }
    }

    return 0;
}
