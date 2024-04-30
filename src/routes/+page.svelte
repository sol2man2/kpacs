<script>
	import { Pane, Splitpanes } from 'svelte-splitpanes';
</script>

<Splitpanes style="height: 1000px" horizontal dblClickSplitter={false}>
	<Pane size={5} minSize={5} maxSize={5}>
		<p>menu bar</p>
	</Pane>
	<Pane size={5} minSize={5} maxSize={5}>
		<p>tool bar</p>
	</Pane>
	<Pane size={55} minSize={45} maxSize={65}>
		<Splitpanes>
			<Pane size={60} minSize={40} maxSize={70}>
				<p>left top</p>
			</Pane>
			<Pane size={40} minSize={30} maxSize={60}>
				<p>right top</p>
			</Pane>
		</Splitpanes>
	</Pane>
	<Pane size={30} minSize={20} maxSize={40}>
		<Splitpanes>
			<Pane size={40} minSize={20} maxSize={50}>
				<p>left bottom</p>
			</Pane>
			<Pane size={30} minSize={20} maxSize={40}>
				<p>center bottom</p>
			</Pane>
			<Pane size={30} minSize={10} maxSize={40}>
				<p>right bottom</p>
			</Pane>
		</Splitpanes>
	</Pane>
	<Pane size={5} minSize={5} maxSize={5}>
		<p>footer</p>
	</Pane>
</Splitpanes>
