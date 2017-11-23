<template>
   <div class="row">
        <div class="col-sm-12 table-responsive">
            <table class="table table-striped">
                <tbody>
                    <tr>
                        <th style="width: 10px">#</th>
                        <th>Name</th>
                        <th>Description</th>
                        <th style="width: 40px">Action</th>
                    </tr>
                    <tr>
                        <td>1.</td>
                        <td>
                            <div>Articles 1</div>
                        </td>
                        <td>
                            <div>Blabh alal baoij ds .....</div>
                        </td>
                        <td>
                            <button type="button" name="Edit" >Edit</button>
                            <button type="button" name="Edit" >Delete</button>
                        </td>
                    </tr>
                   
                </tbody>
            </table>
        </div>
    </div>
</template>

<script>
export default {
 data () {
    return {
      articles : [
          {
              id : 1,
              name: 'article 1',
              desc: 'fadsfdas dsadsa'              
          }
      ]
    }
  },
  mounted() {
    this.$nextTick(() => {});
  }
};
</script>

<style>

</style>


