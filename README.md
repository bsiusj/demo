# demo
//This is my first Git Repository.
//Author- Sujata Khadka

#include <iostream>
using namespace std;

void averages(int score1, int score2, int score3, double& averageAll, double& averageBest) {
    averageAll = (score1 + score2 + score3) / 3.0;

    // Find the two best scores
    int lowestScore = min(score1, min(score2, score3));
    averageBest = (score1 + score2 + score3 - lowestScore) / 2.0;
}

int main() {
    int score1, score2, score3;
    double averageAll, averageBest;

    // Input test scores
    cout << "Enter the first test score: ";
    cin >> score1;

    cout << "Enter the second test score: ";
    cin >> score2;

    cout << "Enter the third test score: ";
    cin >> score3;

    // Compute averages
    averages(score1, score2, score3, averageAll, averageBest);

    // Output the averages
    cout << "Average of all 3 test scores: " << averageAll << endl;
    cout << "Average of the 2 best test scores: " << averageBest << endl;

    return 0;
}
