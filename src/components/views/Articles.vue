<template>
    <div class="articles-container">
        <div class="row">
            <div class="col-sm-6">
                <form class="form-add-articles" v-on:submit="submit">
                    <div class="form-group">
                        <input type="text" class="form-control" placeholder="Enter Name ..." v-model="artName" />
                    </div>
                    <div class="form-group">
                        <input type="text" class="form-control" placeholder="Description ..." v-model="artDesc" />
                    </div>
                    <button type="submit" class="btn btn-default">Add</button>
                </form>
            </div>
        </div>
        <div class="row">
            <div class="col-sm-12"> 
                <image-uploader name="fooImport" @files="selectedFile" :show="true" :showNative="true" />
            </div>
        </div>
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
                        <tr v-for="item in articles">
                            <td><div>{{ item.id}}</div></td>
                            <td><div>{{ item.name}}</div></td>
                            <td><div>{{ item.desc}}</div></td>
                            <td>
                                <button type="button" name="Edit">Edit</button>
                                <button type="button" name="Delete">Delete</button>
                            </td>
                        </tr>

                    </tbody>
                </table>
            </div>
        </div>
    </div>
</template>

<script>
import ImageUploader from '../ImageUploader';

    export default {
        components: { ImageUploader },
        props: {
            artName: { type: String, default: "" },
            artDesc: { type: String, default: "" }
        },
        data() {
            return {
                articles: [
                    {
                        id: 1,
                        name: 'article 1',
                        desc: 'fadsfdas dsadsa'
                    }
                ]
            }
        },
        mounted() {
            this.$nextTick(() => { });
        },
        methods: {
            submit: function (e) {
                alert(this.sName);
                e.preventDefault();
                debugger;
                this.articles.push({
                    id: 2,
                    name: this.artName,
                    desc: this.artDesc
                });
            },
            selectedFile: function(data) {
                console.log('selectedFile');
                console.log(data);
            }
        }
    };

</script>

<style>
    .form-add-articles {
        border: dashed 2px saddlebrown;
        padding: 20px;
    }
</style>