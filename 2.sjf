#include<stdio.h>
void main() {
 int pid[10], bt[10], wt[10], tat[10], n, twt = 0, ttat = 0, i, j, t;
 float awt, atat;
 printf("Enter no. of processes:");
 scanf("%d", &n);
 printf("\nEnter burst times:\n");
 for (i = 0; i < n; i++) {
 scanf("%d", &bt[i]);
 }
 printf("\nEnter PID:\n");
 for (i = 0; i < n; i++) {
 scanf("%d", &pid[i]);
 }
 // Sorting processes based on burst time using Bubble Sort
 for (i = 0; i < n; i++) {
 for (j = i + 1; j < n; j++) {
 if (bt[i] > bt[j]) {
 t = bt[i];
 bt[i] = bt[j];
 bt[j] = t;
 t = pid[i];
 pid[i] = pid[j];
 pid[j] = t;
 }
 }
 }
 wt[0] = 0;
 tat[0] = bt[0];
 // Calculating waiting time and turnaround time
 for (i = 1; i < n; i++) {
 wt[i] = tat[i - 1];
 tat[i] = bt[i] + wt[i];
 }
 // Calculating total waiting time and total turnaround time
 for (i = 0; i < n; i++) {
 ttat += tat[i];
 twt += wt[i];
 }
 printf("\nPID \tBT \tWT \tTAT\n");
 for (i = 0; i < n; i++) {
 printf("%d \t%d \t%d \t%d\n", pid[i], bt[i], wt[i], tat[i]);
 }
 awt = (float)twt / n;
 atat = (float)ttat / n;
 printf("\nAvg. Waiting Time = %f", awt);
 printf("\nAvg. Turnaround Time = %f\n", atat);
}
