#include <iostream>
#include <string>
#include <vector>
#include <algorithm>

using namespace std;
int findIndex(int w, int h, vector<string> & vector, int cloumn);
/**
* Auto-generated code below aims at helping you parse
* the standard input according to the problem statement.
**/
int main()
{
	int W;
	int H;
	cin >> W >> H; cin.ignore();
	cerr << "W: " << W << ", H: " << H << endl;
	vector<string> vector;
	string top;
	string bottom;
	for (int i = 0; i < H; i++) {
		string line;
		getline(cin, line);
		vector.push_back(line);
		cerr << "line: " << line << endl;
		if (i == 0)	top = line;
		if (i == H - 1)	bottom = line;
	}
	char str[2];
	for (int i = 0; i < top.size(); i += 3)
	{
		str[0] = top[i];
		int second_index = findIndex(W, H, vector, i);
		str[1] = bottom[second_index];
		cout << str[0] << str[1] << endl;
	}
	system("pause");
	return 0;
}

int findIndex(int w, int h, vector<string> & vector, int cloumn)
{
	int current_index = cloumn;
	string line = "";
	std::vector<string>::iterator it;
	for (it = vector.begin() + 1;it != vector.end(); it++)
	{
		if ((it + 1) == vector.end())
		{
			return current_index;
		}
		line = *it;
		if (current_index + 1 < w - 1 && line[current_index + 1 ] == '-' )
		{
			current_index += 3;
		}
		else if (current_index - 1 >= 0 && line[current_index - 1] == '-')
		{
			current_index -= 3;
		}
		if (current_index - 1 < 0)
			current_index = 0;
		if (current_index > (w - 1))
			current_index = w - 1;
	}
}
