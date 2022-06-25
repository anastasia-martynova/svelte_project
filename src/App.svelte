<script lang="ts">
	import {Tabs, Tab, TabList, TabPanel} from 'svelte-tabs';
    import Facts from './components/facts.svelte';
	import Intro from "./components/intro.svelte";
	import Contacts from "./components/contacts.svelte";

</script>

<Tabs>
    <TabList>
        <Tab>Home</Tab>
        <Tab>About</Tab>
		<Tab>Contacts</Tab>
    </TabList>

    <TabPanel>
        <main>
            <Intro/>
        </main>
    </TabPanel>

    <TabPanel>
        <main>
            <Facts/>
        </main>
    </TabPanel>

	<TabPanel>
        <main>
            <Contacts/>
        </main>
    </TabPanel>
</Tabs>

<style>
	
	:global(.svelte-tabs div.svelte-tabs__tab-panel){
		margin-top: 0em;
	}
	:global(.svelte-tabs__tab-list) {
		padding-left: 100px;
		margin-top: 0em;
		max-width:initial;
		margin: 0 auto;
		max-height: 100%;
		position: fixed;
		top: 0;
		left: 0;
		width: 100%;
		display: flex;				
		flex-wrap: wrap;
		align-items: flex-end;
		margin-right: 80px;

    }
	:global(.svelte-tabs li.svelte-tabs__tab){
		padding-top: 0px;
		margin-left: 50px;
		font-size: 18px;
		line-height: 24px;
		color: white;
		text-decoration: none;
	}
</style>