<template>
  <div>
    <Accordion type="single" collapsible>
      <AccordionItem value="item-1">
        <AccordionTrigger class="bg-gray-200 px-4 py-2 rounded-md">Is it accessible?</AccordionTrigger>
        <AccordionContent class="bg-white p-4">
          Yes. It adheres to the WAI-ARIA design pattern.
        </AccordionContent>
      </AccordionItem>
    </Accordion>
    <Button class="bg-blue-700 px-4 py-2 rounded-md text-white mt-4">Button</Button>
    <Calendar v-model="value" :weekday-format="'short'" class="rounded-md border items-center bg-blue-500" />
  </div>
</template>

<script setup lang="ts">
  import { Accordion, AccordionContent, AccordionItem, AccordionTrigger } from '@/components/ui/accordion'
  import { Button } from '@/components/ui/button'
  import { type DateValue, getLocalTimeZone, today } from '@internationalized/date'
import { Calendar } from '@/components/ui/calendar'

const value = ref(today(getLocalTimeZone())) as Ref<DateValue>
</script>

<style>

</style>
