# Mravi
Solución al problema Mravi del sitio web Kattis - Estudiantes UDABOL2022-02

from heapq import heappop, heappush
from math import sqrt


class MaxHeap:
    @staticmethod
    def construct_init_heap_from_input():
        heap = MaxHeap()
        for v, init_cost in enumerate(map(int, input().split())):
            if init_cost != -1:
                heap.push(v, init_cost)
        return heap
