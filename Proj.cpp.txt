#include <iostream>

int main()
{
setlocale(LC_ALL, "Rus");
	struct product
	{
		char sName[30];
		int quantity;
		int price;
		char manufacturer[30];
		int date[3];
	};
	const int  n = 10;
	short ind;
	product tproduct[n];
	int tmp = -10000;
	for (int i = 0; i < n; i++) 
	{
		if ((tproduct[i].quantity * tproduct[i].price) > tmp) 
		{
			tmp = tproduct[i].quantity * tproduct[i].price;
			ind = i;
		}

	}
	std::cout<<tproduct[ind].sName;
	std::cin.get();
	return 0;
}