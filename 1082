#include <stdio.h>
#include <stdlib.h>

typedef struct {
  char ID[5];
  int x;
  int y;
  long long check;
}info;

int cmp(const void *a, const void *b){
  info *aa = (info *)a;
  info *bb = (info *)b;
  return aa->check - bb->check;
}

int main(int argc, char *argv[]){
  int n, i;
  scanf("%d", &n);
  info in[n];
  for(i=0; i<n; i++){
    scanf("%s %d %d", in[i].ID, &in[i].x, &in[i].y);
    in[i].check=in[i].x*in[i].x+in[i].y*in[i].y;
  }
  qsort(in, n, sizeof(info), cmp);
  printf("%s %s\n", in[0].ID, in[n-1].ID);
  return 0;
}
