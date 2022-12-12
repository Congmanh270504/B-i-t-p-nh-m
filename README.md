# Texting
#include<conio.h>
#include<stdio.h>

void nhap(int a[], int n)
{

	for (int i = 0; i < n; i++)
	{
		printf("a[%d]=", i);

		scanf_s("%d", &a[i]);
	}

}
void xuat(int a[], int n)
{
	printf("Chuoi vua nhap la: ");
	for (int i = 0; i < n; i++)
	{
		printf("\t%d", a[i]);

	}
	printf("\n");
}
//void hoanvi(int d, int f)
//{
//	int c = d;
//	 d = f; f = c;
//
//}

void mangtang(int a[], int n)
{
	int tg;


	for (int i = 0; i <= n - 1; i++)
	{
		for (int j = i + 1; j < n; j++) {
			if (a[i] > a[j]) {
				// Hoan vi 2 so a[i] va a[j]
				tg = a[i];
				a[i] = a[j];
				a[j] = tg;
			}
		}
		printf("%d", a[i]);
	}
	printf("\n");
}
int tim(int a[], int n, int x)
{
	for (int i = 0; i < n; i++)
	{
		if (a[i] == x)
			printf("a[%d]", i);
	}
	return 0;

}
void insert(int a[], int& n, int x) {
	int i;
	i = n++;
	while (x < a[i - 1]) {
		a[i] = a[i - 1];
		a[i] = x;
		
	}

}



int main()
{
	int  a[1000];
	int b[] = { 1,3,4,5 };
	int x, n, d, f;

	printf("Nhap so luong phan tu mang: ");
	scanf_s("%d", &n);
	nhap(a, n);
	xuat(a, n);
	mangtang(a, n);
	printf("Nhap x: ");
	scanf_s("%d", &x);
	tim(a, n, x);
	insert(a, n, x);
	_getch();


}
