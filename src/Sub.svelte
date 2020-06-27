<script>
  import { createEventDispatcher } from 'svelte'

  const dispatch = createEventDispatcher()

  dispatch('ev', { my: 'event' })
</script>