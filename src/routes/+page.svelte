<script lang="ts">
 import * as Drawer from "$lib/components/ui/drawer";

import * as DropdownMenu from "$lib/components/ui/dropdown-menu";

 let open = $state(false)
 let open2 = $state(false)
 $inspect(open, 'Drop')
 $inspect(open2, 'draw')
 
 </script>


 

 <div class="w-full flex justify-center items-center h-screen">
<DropdownMenu.Root bind:open={open}>
  <DropdownMenu.Trigger class="bg-gray-500 p-4 rounded-lg">Open</DropdownMenu.Trigger>
  <DropdownMenu.Content interactOutsideBehavior="defer-otherwise-close">
    <DropdownMenu.Group>
      <DropdownMenu.GroupHeading>My Account</DropdownMenu.GroupHeading>
      <DropdownMenu.Separator />
   <DropdownMenu.Item onclick={() => open2 = true}>
      Click me
   </DropdownMenu.Item>
    </DropdownMenu.Group>
  </DropdownMenu.Content>
</DropdownMenu.Root></div>


<Drawer.Root bind:open={open2} >
 <Drawer.Trigger ></Drawer.Trigger>
 <Drawer.Content interactOutsideBehavior="close" >
  <Drawer.Header>
   <Drawer.Title>Are you sure absolutely sure?</Drawer.Title>
   <Drawer.Description>This action cannot be undone.</Drawer.Description>
  </Drawer.Header>
  <Drawer.Footer>
   <Drawer.Close>Cancel</Drawer.Close>
  </Drawer.Footer>
 </Drawer.Content>
</Drawer.Root>