<script>
  import FriendAdder from './FriendAdder.svelte'
  import LoadFriendList from './LoadFriendList.svelte'
  import QuerryLoadFriendList from './QuerryLoad-FriendList.svelte'
  import QuerryNameFriendsList from './QuerryName-FriendsList.svelte'
</script>

<h4>My simple Dexie app</h4>
<FriendAdder />
<hr />

<div class="p-3">
  <h2>Result</h2>
  <div class="flex justify-around">
    <div><QuerryLoadFriendList /></div>
    <div><LoadFriendList /></div>
    <div><QuerryNameFriendsList /></div>
  </div>
</div>
