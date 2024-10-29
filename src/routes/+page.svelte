<script lang="ts">
 import * as Drawer from "$lib/components/ui/drawer";
  import {
  Button
 } from "$lib/components/ui/button/index.js";
 import * as Dialog from "$lib/components/ui/dialog/index.js";
 let open = $state(false)

</script>
 
<Drawer.Root  bind:open>
 <Drawer.Trigger ></Drawer.Trigger>
 <Drawer.Content>
  <Drawer.Header>
   <Drawer.Title>Are you sure absolutely sure?</Drawer.Title>
   <Drawer.Description>This action cannot be undone.</Drawer.Description>
  </Drawer.Header>
  <Drawer.Footer>
   <Drawer.Close>Cancel</Drawer.Close>
  </Drawer.Footer>
 </Drawer.Content>
</Drawer.Root>

 
<Dialog.Root >
 <Dialog.Trigger  class="bg-gray-400 rounded p-4 "
>Edit Profile</Dialog.Trigger
 >
 <Dialog.Content class="sm:max-w-[425px]">
  <Dialog.Header>
   <Dialog.Title>Edit profile</Dialog.Title>
   <Dialog.Description>
    Make changes to your profile here. Click save when you're done.
   </Dialog.Description>
  </Dialog.Header>
  <div class="grid gap-4 py-4">
    <Button onclick={() => open = true} class="text-right">Open Drawer</Button>
  </div>
  <Dialog.Footer>
  </Dialog.Footer>
 </Dialog.Content>
</Dialog.Root>