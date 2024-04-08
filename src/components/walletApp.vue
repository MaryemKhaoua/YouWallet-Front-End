<template>
    <div class="d-flex justify-content-center container text-white mt-5">
        <div class="card p-2 px-3 py-3">
            <div class="d-flex justify-content-between align-items-center"><button class="btn"  width="20" height="20">visa</button></div>
            <div class="mt-3"><span class="mr-3">****</span><span class="mr-3">****</span><span class="mr-3">****</span><span class="mr-2">5513</span></div>
            <div class="d-flex justify-content-between card-details mt-3 mb-3">
                <div class="d-flex flex-column"><span class="light">Card Holder</span><span>Sam Dingo</span></div>
                <div class="d-flex flex-row">
                    <div class="d-flex flex-column mr-3"><span class="light">Expired</span><span>12/24</span></div>
                    <div class="d-flex flex-column"><span class="light">CVV</span><span>857</span></div>
                </div>
            </div>
        </div>
    </div>
<div class="btn">
    <button class="btn btn-success">Add Card</button>
</div>
</template>
<style scoped>
.card {
  position: relative;
  display: flex;
  width: 395px;
  flex-direction: column;
  min-width: 0;
  word-wrap: break-word;
  background-color: #678dc9;
  background-clip: border-box;
  border: 1px solid #8595b0;
  border-radius: 7px;
}

.light {
  color: #462c2c;
  font-size: 11px;
}
</style>

<script>



</script>