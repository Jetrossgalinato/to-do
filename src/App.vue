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
</script>

<template>
  <div class="flex min-h-screen items-center justify-center bg-gray-100">
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
      ><CardFooter></CardFooter>
    </Card>
  </div>
</template>
