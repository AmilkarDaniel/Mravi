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
    def _init_(self):
        self.h = []

    def push(self, v, cost):
        heappush(self.h, (-cost,v))

    def pop(self):
        cost, v = heappop(self.h)
        return -cost, v

    def _bool_(self):
        return bool(self.h)
class Graph:
    @staticmethod
    def construct_from_input():
        g = Graph(int(input()))
        for _ in range(len(g.vertices) - 1)
            g.add_parent(*map(int, input().split()))
        return g
