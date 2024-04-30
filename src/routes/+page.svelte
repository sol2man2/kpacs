<script>
    import { fly } from 'svelte/transition'

	import { Pane, Splitpanes } from 'svelte-splitpanes';
    import { Svroller } from 'svrollbar'

    import { Table, TableBody, TableBodyCell, TableBodyRow, TableHead, TableHeadCell, Checkbox, TableSearch } from 'flowbite-svelte';

    const items = Array.from({ length: 50 }).map((_, i) => `item ${i}`)
    const flyLeft = (node) => fly(node, { x: -160 })
    const flyRight = (node) => fly(node, { x: 30 })
</script>

<Splitpanes style="height: 1000px" horizontal dblClickSplitter={false}>
	<Pane size={5} minSize={5} maxSize={5}>
		<p>menu bar</p>
	</Pane>
	<Pane size={5} minSize={5} maxSize={5}>
        <span>Preset</span>
        <select><option value="0">--</option><option value="1">default</option><option value="2">1w xr</option></select>
        <button>Save</button> <button>Delete</button>
        <span>Dates</span>
        <select><option value="0">any</option><option value="1">1w</option><option value="2">2w</option><option value="2">1m</option><option value="2">1q</option><option value="2">1h</option><option value="2">1y</option></select>
        <span>Modality</span>
        <select><option value="0">xr</option><option value="1">ct</option><option value="2">mr</option></select>
        <span>Body Parts</span>
        <select><option value="0">brain</option><option value="1">chest</option><option value="2">abdomen</option></select>
        <span>Search</span>
        <input type="text" />
        <button>search</button>
	</Pane>
	<Pane size={55} minSize={45} maxSize={65}>
		<Splitpanes>
			<Pane size={70} minSize={40} maxSize={70}>
                <div class="container">
                    <Svroller
                      width="65rem"
                      height="30rem"
                      hideAfter={1000}
                      vTrackIn={flyLeft}
                      vTrackOut={flyLeft}
                      vThumbIn={flyRight}
                      vThumbOut={flyRight}>

                      <Table>
                        <TableHead>
                          <TableHeadCell>Study Date Time</TableHeadCell>
                          <TableHeadCell>Patient ID Issuer</TableHeadCell>
                          <TableHeadCell>Patient ID</TableHeadCell>
                          <TableHeadCell>Patient Name</TableHeadCell>
                          <TableHeadCell>Sex</TableHeadCell>
                          <TableHeadCell>Date of Birth</TableHeadCell>
                          <TableHeadCell>Accession number</TableHeadCell>
                          <TableHeadCell>Modality</TableHeadCell>
                          <TableHeadCell>Study ID</TableHeadCell>
                          <TableHeadCell>Study Description</TableHeadCell>
                          <TableHeadCell>Body Parts</TableHeadCell>
                          <TableHeadCell>Study Instance UID</TableHeadCell>
                          <TableHeadCell>Created Date Time</TableHeadCell>
                        </TableHead>
                        <TableHead>
                            <TableHeadCell><select name="languages" id="lang">
                                <option value="1">one</option><option value="2">two</option><option value="3">three</option><option value="4">four</option>
                            </select></TableHeadCell>
                            <TableHeadCell><select name="languages" id="lang">
                                <option value="1">one</option><option value="2">two</option><option value="3">three</option><option value="4">four</option>
                            </select></TableHeadCell>
                            <TableHeadCell><select name="languages" id="lang">
                                <option value="1">one</option><option value="2">two</option><option value="3">three</option><option value="4">four</option>
                            </select></TableHeadCell>
                            <TableHeadCell><select name="languages" id="lang">
                                <option value="1">one</option><option value="2">two</option><option value="3">three</option><option value="4">four</option>
                            </select></TableHeadCell>
                            <TableHeadCell><select name="languages" id="lang">
                                <option value="1">one</option><option value="2">two</option><option value="3">three</option><option value="4">four</option>
                            </select></TableHeadCell>
                            <TableHeadCell><select name="languages" id="lang">
                                <option value="1">one</option><option value="2">two</option><option value="3">three</option><option value="4">four</option>
                            </select></TableHeadCell>
                            <TableHeadCell><select name="languages" id="lang">
                                <option value="1">one</option><option value="2">two</option><option value="3">three</option><option value="4">four</option>
                            </select></TableHeadCell>
                            <TableHeadCell><select name="languages" id="lang">
                                <option value="1">one</option><option value="2">two</option><option value="3">three</option><option value="4">four</option>
                            </select></TableHeadCell>
                            <TableHeadCell><select name="languages" id="lang">
                                <option value="1">one</option><option value="2">two</option><option value="3">three</option><option value="4">four</option>
                            </select></TableHeadCell>
                            <TableHeadCell><select name="languages" id="lang">
                                <option value="1">one</option><option value="2">two</option><option value="3">three</option><option value="4">four</option>
                            </select></TableHeadCell>
                            <TableHeadCell><select name="languages" id="lang">
                                <option value="1">one</option><option value="2">two</option><option value="3">three</option><option value="4">four</option>
                            </select></TableHeadCell>
                            <TableHeadCell><select name="languages" id="lang">
                                <option value="1">one</option><option value="2">two</option><option value="3">three</option><option value="4">four</option>
                            </select></TableHeadCell>
                            <TableHeadCell><select name="languages" id="lang">
                                <option value="1">one</option><option value="2">two</option><option value="3">three</option><option value="4">four</option>
                            </select></TableHeadCell>

                        </TableHead>
                        <TableBody tableBodyClass="divide-y">
                          <TableBodyRow>
                            <TableBodyCell>1</TableBodyCell>
                            <TableBodyCell>2</TableBodyCell>
                            <TableBodyCell>3</TableBodyCell>
                            <TableBodyCell>4</TableBodyCell>
                            <TableBodyCell>5</TableBodyCell>
                            <TableBodyCell>6</TableBodyCell>
                            <TableBodyCell>7</TableBodyCell>
                            <TableBodyCell>8</TableBodyCell>
                            <TableBodyCell>9</TableBodyCell>
                            <TableBodyCell>10</TableBodyCell>
                            <TableBodyCell>11</TableBodyCell>
                            <TableBodyCell>12</TableBodyCell>
                            <TableBodyCell>13</TableBodyCell>
                          </TableBodyRow>
                          <TableBodyRow>
                            <TableBodyCell>2</TableBodyCell>
                            <TableBodyCell>3</TableBodyCell>
                            <TableBodyCell>4</TableBodyCell>
                            <TableBodyCell>5</TableBodyCell>
                            <TableBodyCell>6</TableBodyCell>
                            <TableBodyCell>7</TableBodyCell>
                            <TableBodyCell>8</TableBodyCell>
                            <TableBodyCell>9</TableBodyCell>
                            <TableBodyCell>10</TableBodyCell>
                            <TableBodyCell>11</TableBodyCell>
                            <TableBodyCell>12</TableBodyCell>
                            <TableBodyCell>13</TableBodyCell>
                            <TableBodyCell>14</TableBodyCell>
                          </TableBodyRow>
                          <TableBodyRow>
                            <TableBodyCell>1</TableBodyCell>
                            <TableBodyCell>2</TableBodyCell>
                            <TableBodyCell>3</TableBodyCell>
                            <TableBodyCell>4</TableBodyCell>
                            <TableBodyCell>5</TableBodyCell>
                            <TableBodyCell>6</TableBodyCell>
                            <TableBodyCell>7</TableBodyCell>
                            <TableBodyCell>8</TableBodyCell>
                            <TableBodyCell>9</TableBodyCell>
                            <TableBodyCell>10</TableBodyCell>
                            <TableBodyCell>11</TableBodyCell>
                            <TableBodyCell>12</TableBodyCell>
                            <TableBodyCell>13</TableBodyCell>
                          </TableBodyRow>
                          <TableBodyRow>
                            <TableBodyCell>2</TableBodyCell>
                            <TableBodyCell>3</TableBodyCell>
                            <TableBodyCell>4</TableBodyCell>
                            <TableBodyCell>5</TableBodyCell>
                            <TableBodyCell>6</TableBodyCell>
                            <TableBodyCell>7</TableBodyCell>
                            <TableBodyCell>8</TableBodyCell>
                            <TableBodyCell>9</TableBodyCell>
                            <TableBodyCell>10</TableBodyCell>
                            <TableBodyCell>11</TableBodyCell>
                            <TableBodyCell>12</TableBodyCell>
                            <TableBodyCell>13</TableBodyCell>
                            <TableBodyCell>14</TableBodyCell>
                          </TableBodyRow>
                          <TableBodyRow>
                            <TableBodyCell>1</TableBodyCell>
                            <TableBodyCell>2</TableBodyCell>
                            <TableBodyCell>3</TableBodyCell>
                            <TableBodyCell>4</TableBodyCell>
                            <TableBodyCell>5</TableBodyCell>
                            <TableBodyCell>6</TableBodyCell>
                            <TableBodyCell>7</TableBodyCell>
                            <TableBodyCell>8</TableBodyCell>
                            <TableBodyCell>9</TableBodyCell>
                            <TableBodyCell>10</TableBodyCell>
                            <TableBodyCell>11</TableBodyCell>
                            <TableBodyCell>12</TableBodyCell>
                            <TableBodyCell>13</TableBodyCell>
                          </TableBodyRow>
                          <TableBodyRow>
                            <TableBodyCell>2</TableBodyCell>
                            <TableBodyCell>3</TableBodyCell>
                            <TableBodyCell>4</TableBodyCell>
                            <TableBodyCell>5</TableBodyCell>
                            <TableBodyCell>6</TableBodyCell>
                            <TableBodyCell>7</TableBodyCell>
                            <TableBodyCell>8</TableBodyCell>
                            <TableBodyCell>9</TableBodyCell>
                            <TableBodyCell>10</TableBodyCell>
                            <TableBodyCell>11</TableBodyCell>
                            <TableBodyCell>12</TableBodyCell>
                            <TableBodyCell>13</TableBodyCell>
                            <TableBodyCell>14</TableBodyCell>
                          </TableBodyRow>
                          <TableBodyRow>
                            <TableBodyCell>1</TableBodyCell>
                            <TableBodyCell>2</TableBodyCell>
                            <TableBodyCell>3</TableBodyCell>
                            <TableBodyCell>4</TableBodyCell>
                            <TableBodyCell>5</TableBodyCell>
                            <TableBodyCell>6</TableBodyCell>
                            <TableBodyCell>7</TableBodyCell>
                            <TableBodyCell>8</TableBodyCell>
                            <TableBodyCell>9</TableBodyCell>
                            <TableBodyCell>10</TableBodyCell>
                            <TableBodyCell>11</TableBodyCell>
                            <TableBodyCell>12</TableBodyCell>
                            <TableBodyCell>13</TableBodyCell>
                          </TableBodyRow>
                          <TableBodyRow>
                            <TableBodyCell>2</TableBodyCell>
                            <TableBodyCell>3</TableBodyCell>
                            <TableBodyCell>4</TableBodyCell>
                            <TableBodyCell>5</TableBodyCell>
                            <TableBodyCell>6</TableBodyCell>
                            <TableBodyCell>7</TableBodyCell>
                            <TableBodyCell>8</TableBodyCell>
                            <TableBodyCell>9</TableBodyCell>
                            <TableBodyCell>10</TableBodyCell>
                            <TableBodyCell>11</TableBodyCell>
                            <TableBodyCell>12</TableBodyCell>
                            <TableBodyCell>13</TableBodyCell>
                            <TableBodyCell>14</TableBodyCell>
                          </TableBodyRow>
                          <TableBodyRow>
                            <TableBodyCell>1</TableBodyCell>
                            <TableBodyCell>2</TableBodyCell>
                            <TableBodyCell>3</TableBodyCell>
                            <TableBodyCell>4</TableBodyCell>
                            <TableBodyCell>5</TableBodyCell>
                            <TableBodyCell>6</TableBodyCell>
                            <TableBodyCell>7</TableBodyCell>
                            <TableBodyCell>8</TableBodyCell>
                            <TableBodyCell>9</TableBodyCell>
                            <TableBodyCell>10</TableBodyCell>
                            <TableBodyCell>11</TableBodyCell>
                            <TableBodyCell>12</TableBodyCell>
                            <TableBodyCell>13</TableBodyCell>
                          </TableBodyRow>
                          <TableBodyRow>
                            <TableBodyCell>2</TableBodyCell>
                            <TableBodyCell>3</TableBodyCell>
                            <TableBodyCell>4</TableBodyCell>
                            <TableBodyCell>5</TableBodyCell>
                            <TableBodyCell>6</TableBodyCell>
                            <TableBodyCell>7</TableBodyCell>
                            <TableBodyCell>8</TableBodyCell>
                            <TableBodyCell>9</TableBodyCell>
                            <TableBodyCell>10</TableBodyCell>
                            <TableBodyCell>11</TableBodyCell>
                            <TableBodyCell>12</TableBodyCell>
                            <TableBodyCell>13</TableBodyCell>
                            <TableBodyCell>14</TableBodyCell>
                          </TableBodyRow>
                          <TableBodyRow>
                            <TableBodyCell>1</TableBodyCell>
                            <TableBodyCell>2</TableBodyCell>
                            <TableBodyCell>3</TableBodyCell>
                            <TableBodyCell>4</TableBodyCell>
                            <TableBodyCell>5</TableBodyCell>
                            <TableBodyCell>6</TableBodyCell>
                            <TableBodyCell>7</TableBodyCell>
                            <TableBodyCell>8</TableBodyCell>
                            <TableBodyCell>9</TableBodyCell>
                            <TableBodyCell>10</TableBodyCell>
                            <TableBodyCell>11</TableBodyCell>
                            <TableBodyCell>12</TableBodyCell>
                            <TableBodyCell>13</TableBodyCell>
                          </TableBodyRow>
                          <TableBodyRow>
                            <TableBodyCell>2</TableBodyCell>
                            <TableBodyCell>3</TableBodyCell>
                            <TableBodyCell>4</TableBodyCell>
                            <TableBodyCell>5</TableBodyCell>
                            <TableBodyCell>6</TableBodyCell>
                            <TableBodyCell>7</TableBodyCell>
                            <TableBodyCell>8</TableBodyCell>
                            <TableBodyCell>9</TableBodyCell>
                            <TableBodyCell>10</TableBodyCell>
                            <TableBodyCell>11</TableBodyCell>
                            <TableBodyCell>12</TableBodyCell>
                            <TableBodyCell>13</TableBodyCell>
                            <TableBodyCell>14</TableBodyCell>
                          </TableBodyRow>
                          <TableBodyRow>
                            <TableBodyCell>1</TableBodyCell>
                            <TableBodyCell>2</TableBodyCell>
                            <TableBodyCell>3</TableBodyCell>
                            <TableBodyCell>4</TableBodyCell>
                            <TableBodyCell>5</TableBodyCell>
                            <TableBodyCell>6</TableBodyCell>
                            <TableBodyCell>7</TableBodyCell>
                            <TableBodyCell>8</TableBodyCell>
                            <TableBodyCell>9</TableBodyCell>
                            <TableBodyCell>10</TableBodyCell>
                            <TableBodyCell>11</TableBodyCell>
                            <TableBodyCell>12</TableBodyCell>
                            <TableBodyCell>13</TableBodyCell>
                          </TableBodyRow>
                          <TableBodyRow>
                            <TableBodyCell>2</TableBodyCell>
                            <TableBodyCell>3</TableBodyCell>
                            <TableBodyCell>4</TableBodyCell>
                            <TableBodyCell>5</TableBodyCell>
                            <TableBodyCell>6</TableBodyCell>
                            <TableBodyCell>7</TableBodyCell>
                            <TableBodyCell>8</TableBodyCell>
                            <TableBodyCell>9</TableBodyCell>
                            <TableBodyCell>10</TableBodyCell>
                            <TableBodyCell>11</TableBodyCell>
                            <TableBodyCell>12</TableBodyCell>
                            <TableBodyCell>13</TableBodyCell>
                            <TableBodyCell>14</TableBodyCell>
                          </TableBodyRow>
                          <TableBodyRow>
                            <TableBodyCell>1</TableBodyCell>
                            <TableBodyCell>2</TableBodyCell>
                            <TableBodyCell>3</TableBodyCell>
                            <TableBodyCell>4</TableBodyCell>
                            <TableBodyCell>5</TableBodyCell>
                            <TableBodyCell>6</TableBodyCell>
                            <TableBodyCell>7</TableBodyCell>
                            <TableBodyCell>8</TableBodyCell>
                            <TableBodyCell>9</TableBodyCell>
                            <TableBodyCell>10</TableBodyCell>
                            <TableBodyCell>11</TableBodyCell>
                            <TableBodyCell>12</TableBodyCell>
                            <TableBodyCell>13</TableBodyCell>
                          </TableBodyRow>
                          <TableBodyRow>
                            <TableBodyCell>2</TableBodyCell>
                            <TableBodyCell>3</TableBodyCell>
                            <TableBodyCell>4</TableBodyCell>
                            <TableBodyCell>5</TableBodyCell>
                            <TableBodyCell>6</TableBodyCell>
                            <TableBodyCell>7</TableBodyCell>
                            <TableBodyCell>8</TableBodyCell>
                            <TableBodyCell>9</TableBodyCell>
                            <TableBodyCell>10</TableBodyCell>
                            <TableBodyCell>11</TableBodyCell>
                            <TableBodyCell>12</TableBodyCell>
                            <TableBodyCell>13</TableBodyCell>
                            <TableBodyCell>14</TableBodyCell>
                          </TableBodyRow>
                          <TableBodyRow>
                            <TableBodyCell>1</TableBodyCell>
                            <TableBodyCell>2</TableBodyCell>
                            <TableBodyCell>3</TableBodyCell>
                            <TableBodyCell>4</TableBodyCell>
                            <TableBodyCell>5</TableBodyCell>
                            <TableBodyCell>6</TableBodyCell>
                            <TableBodyCell>7</TableBodyCell>
                            <TableBodyCell>8</TableBodyCell>
                            <TableBodyCell>9</TableBodyCell>
                            <TableBodyCell>10</TableBodyCell>
                            <TableBodyCell>11</TableBodyCell>
                            <TableBodyCell>12</TableBodyCell>
                            <TableBodyCell>13</TableBodyCell>
                          </TableBodyRow>
                          <TableBodyRow>
                            <TableBodyCell>2</TableBodyCell>
                            <TableBodyCell>3</TableBodyCell>
                            <TableBodyCell>4</TableBodyCell>
                            <TableBodyCell>5</TableBodyCell>
                            <TableBodyCell>6</TableBodyCell>
                            <TableBodyCell>7</TableBodyCell>
                            <TableBodyCell>8</TableBodyCell>
                            <TableBodyCell>9</TableBodyCell>
                            <TableBodyCell>10</TableBodyCell>
                            <TableBodyCell>11</TableBodyCell>
                            <TableBodyCell>12</TableBodyCell>
                            <TableBodyCell>13</TableBodyCell>
                            <TableBodyCell>14</TableBodyCell>
                          </TableBodyRow>
                          <TableBodyRow>
                            <TableBodyCell>1</TableBodyCell>
                            <TableBodyCell>2</TableBodyCell>
                            <TableBodyCell>3</TableBodyCell>
                            <TableBodyCell>4</TableBodyCell>
                            <TableBodyCell>5</TableBodyCell>
                            <TableBodyCell>6</TableBodyCell>
                            <TableBodyCell>7</TableBodyCell>
                            <TableBodyCell>8</TableBodyCell>
                            <TableBodyCell>9</TableBodyCell>
                            <TableBodyCell>10</TableBodyCell>
                            <TableBodyCell>11</TableBodyCell>
                            <TableBodyCell>12</TableBodyCell>
                            <TableBodyCell>13</TableBodyCell>
                          </TableBodyRow>
                          <TableBodyRow>
                            <TableBodyCell>2</TableBodyCell>
                            <TableBodyCell>3</TableBodyCell>
                            <TableBodyCell>4</TableBodyCell>
                            <TableBodyCell>5</TableBodyCell>
                            <TableBodyCell>6</TableBodyCell>
                            <TableBodyCell>7</TableBodyCell>
                            <TableBodyCell>8</TableBodyCell>
                            <TableBodyCell>9</TableBodyCell>
                            <TableBodyCell>10</TableBodyCell>
                            <TableBodyCell>11</TableBodyCell>
                            <TableBodyCell>12</TableBodyCell>
                            <TableBodyCell>13</TableBodyCell>
                            <TableBodyCell>14</TableBodyCell>
                          </TableBodyRow>
                        </TableBody>
                      </Table>

                      <!-- {#each items as item (item)}
                        <div>{item}</div>
                      {/each} -->
                    </Svroller>
                  </div>


				<p>left top</p>
			</Pane>
			<Pane size={30} minSize={30} maxSize={60}>
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
