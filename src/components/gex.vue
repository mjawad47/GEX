<template>
	<div>
	 <div class="main-area" id="list-rendering">
	<div class="pressese">
		<h1>GEX: Press Q or ESC To Quit</h1>
	</div>
	<div class="row">
		<div class="col-md-8">
			<div class="row">
				<div class="col-md-3">
					<div class="gex_block">
						<h1>Network</h1>
						<div class="gex_block_inner">
							<p v-for="project in projects">
						      {{ project.text }}
						    </p>
							
						</div>
					</div>
				</div>

				<div class="col-md-3">
					<div class="gex_block">
						<h1>Health</h1>
						<div class="gex_block_inner">
							 <label class='custom-control blue-checkbox' v-for="health in healths">
  <input type='checkbox' class='fill-control-input'>
  <span class='fill-control-indicator'></span>
  {{ health.text }}
</label>
							<dv class="form-check">
							
						</dv>
							
						</div>
					</div>
				</div>

				<div class="col-md-3">
					<div class="gex_block">
						<h1>System time</h1>
						<div class="gex_block_inner">
							<p v-for="system_time in system_times">
						      {{ system_time.text }}

						    </p>
						</div>
					</div>
				</div>

				<div class="col-md-3">
					<div class="gex_block">
						<h1>Connected Peers</h1>
						<div class="gex_block_inner">
							<p v-for="connected_peer in connected_peers">
						      {{ connected_peer.text }}
						    </p>
						</div>
					</div>
				</div>


				<div class="col-md-3">
					<div class="gex_block">
						<h1>Latest BLock</h1>
						<div class="gex_block_inner">
							<p v-for="leatest_block in leatest_blocks">
						      {{ leatest_block.text }}
						    </p>
						</div>
					</div>
				</div>

				<div class="col-md-3">
					<div class="gex_block">
						<h1>Max Block Size</h1>
						<div class="gex_block_inner">
							<p v-for="max_block_size in max_block_sizes">
						      {{ max_block_size.text }}
						    </p>
						</div>
					</div>
				</div>

				<div class="col-md-3">
					<div class="gex_block">
						<h1>S Between Blocks</h1>
						<div class="gex_block_inner">
							<p v-for="between_block in between_blocks">
						      {{ between_block.text }}
						    </p>
						</div>
					</div>
				</div>

				<div class="col-md-3">
					<div class="gex_block">
						<h1>Validators</h1>
						<div class="gex_block_inner">
							<p v-for="validator in validators">
						      {{ validator.text }}
							</p>
						</div>
					</div>
				</div>

				<div class="col-md-3">
					<div class="gex_block">
						<h1>Gas Max</h1>
						<div class="gex_block_inner">
							<p v-for="gas_max in gas_maxs">
						      {{ gas_max.text }}
							</p>
						</div>
					</div>
				</div>

				<div class="col-md-3">
					<div class="gex_block">
						<h1>Gas O block</h1>
						<div class="gex_block_inner">
							<p v-for="gas_o_block in gas_o_blocks">
						      {{ gas_o_block.text }}
							</p>
						</div>
					</div>
				</div>

				<div class="col-md-3">
					<div class="gex_block">
						<h1>Gas O Tx</h1>
						<div class="gex_block_inner">
							<p v-for="gas_o_tx in gas_o_txs">
						      {{ gas_o_tx.text }}
							</p>
						</div>
					</div>
				</div>

				<div class="col-md-3">
					<div class="gex_block">
						<h1>Gas Latest Tx</h1>
						<div class="gex_block_inner">
							<p v-for="gat_latest_tx in gat_latest_txs">
						      {{ gat_latest_tx.text }}
							</p>
						</div>
					</div>
				</div>

			</div>
		</div>
		<div class="col-md-4">
			<div class="gex_block">
						<h1>Current Block Round</h1>
						<div class="gex_block_inner gex_block_inner_right">
							<p v-for="current_block_round in current_block_rounds">
						      {{ current_block_round.text }}
							</p>
						</div>
			</div>

			<div class="gex_block">
						<h1>Latest Confirmed Transactions</h1>
						<div class="gex_block_inner gex_block_inner_right">
							<p v-for="transaction in transactions">
						      {{ transaction.text }}
							</p>
						</div>
			</div>
		</div>
	</div>
</div>
	</div>
</template>


<script>
export default {
	name: 'Navbar',
	data(){
		return {
      userIds: ['1','2','3','4','5','6','7','8',],
       projects: [
        { text: 'Hazlor' },
      ],

      healths: [
        { text: 'Good' },
      ],
      system_times: [
        { text: '2021-10-23' },
        { text: '10:53:02 AM' },
      ],
      connected_peers: [
        { text: 0 },
      ],
      leatest_blocks: [
        { text: 1204 },
      ],
      max_block_sizes: [
        { text: "22.0 MB" },
      ],
      between_blocks : [
        { text: "+Inf seconds" },
      ],
      validators : [
        { text: 1 },
      ],
      gas_maxs : [
        { text: 0 },
      ],
      gas_o_blocks : [
        { text: 0 },
      ],
      gas_o_txs : [
        { text: 0 },
      ],
      gat_latest_txs : [
        { text: 0 },
      ],
      current_block_rounds : [
        { text: "Data" },
      ],
      transactions : [
        { text: "Transactions will appear as soon as they are confirmed in a block." },
      ]
		}
	} 
}	 
</script>

<style scoped>
     body{
        background: red;
        color: #fff;
    }
    .pressese{
    border: 1px solid #008aaa;
    border-radius: 15px;
    padding: 15px;
    background: #182335;
    display: inline-block;
    position: relative;
    top: -44px;
    margin-top: -16px;
    }
    .pressese h1{
        margin: 0px;
        font-size: 20px;
        color: #fff;
    }
    .gex_block_inner p{
        margin-bottom: 5px;
        font-size: 13px;
    }
    .main-area{
    border: 1px solid #008aaa;
    margin: 50px 20px 20px 20px;
    padding: 30px;
    border-radius: 15px;
    }
    .gex_block{
       border: 1px solid #008aaa;
       border-radius: 15px;
       margin-bottom: 20px;

    }
    .gex_block h1{
            padding: 12px 15px;
    font-size: 14px;
    margin: 0px;
    }
    .gex_block_inner{
    border-top: 1px solid #008aaa;
    border-radius: 15px;
    padding: 15px;
    background: #182335;
    min-height: 190px;
    font-size: 14px;
    color: #ccc;
    padding-top: 10px;
    }
    .gex_block_inner_right{
        min-height: 316px;
    }


/* ---- checkbox area ---- */
.blue-checkbox .fill-control-input:checked~.fill-control-indicator{
  background-color: #000000;
  border-color: #0000ff;
}

.fill-control-input{
  display: none;
}
.blue-checkbox .fill-control-input:checked~.fill-control-indicator{
  background-color: #00b321;
    border-color: #00b321;
  background-size: 80%;
}
.fill-control-indicator{
  display: inline-block;
  position: relative;
  top: 3px;
  left: 0;
  width: 15px;
  height: 15px;
  border: 2px solid #aaa;
  transition: .3s;
  background: transperent;
  background-size: 0%;
  background-position: center;
  background-repeat: no-repeat;
  background-image: url("data:image/svg+xml;charset=utf8,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 8 8'%3E%3Cpath fill='%23fff' d='M6.564.75l-3.59 3.612-1.538-1.55L0 4.26 2.974 7.25 8 2.193z'/%3E%3C/svg%3E");
}
	
</style>
