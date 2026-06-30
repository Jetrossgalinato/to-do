<script setup lang="ts">
import {
  Card,
  CardContent,
  CardDescription,
  CardFooter,
  CardHeader,
  CardTitle,
} from "@/components/ui/card";
import {
  Table,
  TableBody,
  TableCell,
  TableHead,
  TableHeader,
  TableRow,
} from "@/components/ui/table";
import { Button } from "@/components/ui/button";
import { Trash2, Pen } from "@lucide/vue";
import ModeToggle from "@/components/ModeToggle.vue";
import {
  Pagination,
  PaginationContent,
  PaginationEllipsis,
  PaginationItem,
  PaginationNext,
  PaginationPrevious,
} from "@/components/ui/pagination";
</script>

<template>
  <div class="absolute top-4 right-4 z-50"><ModeToggle /></div>
  <div class="flex min-h-screen items-center justify-center">
    <Card class="w-[50%]">
      <CardHeader>
        <CardTitle>To-do List</CardTitle>
        <CardDescription>
          A simple to-do list application built with Vue 3 and TypeScript.
        </CardDescription>
      </CardHeader>
      <CardContent>
        <div class="border border-border rounded-md">
          <Table>
            <TableHeader>
              <TableRow>
                <TableHead class="w-[100px]"> Task</TableHead>
                <TableHead>Date & Time</TableHead>
                <TableHead>Status</TableHead>
                <TableHead class="text-right"> Action </TableHead>
              </TableRow>
            </TableHeader>
            <TableBody>
              <TableRow>
                <TableCell class="font-medium">
                  Create this To-do List Application
                </TableCell>
                <TableCell>06/30/2026 21:18</TableCell>
                <TableCell>Pending</TableCell>
                <TableCell class="text-right space-x-2">
                  <Button variant="outline"><Pen /></Button>
                  <Button variant="destructive"><Trash2 /></Button>
                </TableCell>
              </TableRow>
            </TableBody>
          </Table>
        </div> </CardContent
      ><CardFooter class="space-x-2"
        ><Pagination :items-per-page="10">
          <PaginationContent>
            <PaginationItem :value="0">
              <PaginationPrevious href="#" />
            </PaginationItem>
            <PaginationItem :value="1">
              <PaginationLink href="#"> 1 </PaginationLink>
            </PaginationItem>
            <PaginationItem :value="2">
              <PaginationLink href="#" is-active> 2 </PaginationLink>
            </PaginationItem>
            <PaginationItem :value="3">
              <PaginationLink href="#"> 3 </PaginationLink>
            </PaginationItem>
            <PaginationItem :value="4">
              <PaginationEllipsis />
            </PaginationItem>
            <PaginationItem :value="5">
              <PaginationNext href="#" />
            </PaginationItem>
          </PaginationContent> </Pagination
      ></CardFooter>
    </Card>
  </div>
</template>
