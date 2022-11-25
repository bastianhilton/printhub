<template>
  <div>
    <form @submit.prevent="addWHID">
      <nav class="navbar navbar-dark bg-dark">
        <div class="container-fluid">
          <a class="navbar-brand">
            <button type="reset" class="btn btn-warning">Reset</button></a>
          <a class="navbar-brand">
            <input type="submit" class="btn btn-warning" value="Save WHID" /></a>
        </div>
      </nav>
      <br>
      <div class="row">
        <div class="col-3">
          <!-- Tab navs -->
          <div id="v-tabs-tab" class="nav flex-column nav-tabs text-center" role="tablist" aria-orientation="vertical">
            <a id="v-tabs-home-tab" class="nav-link active" data-mdb-toggle="tab" href="#v-tabs-home" role="tab"
              aria-controls="v-tabs-home" aria-selected="true">Create A New WHID</a>
          </div>
          <!-- Tab navs -->
        </div>

        <div class="col-9">
          <div id="v-tabs-tabContent" class="tab-scope">
            <div id="v-tabs-home" class="tab-pane fade show active" role="tabpanel" aria-labelledby="v-tabs-home-tab">
              <div class="table table-responsive">
                <table class="table">
                  <tbody class="row">
                    <tr class="col-lg-6">
                      <td>
                        <label for="name">WHID Name</label><br>
                        <input type="text" required value="WHID Name" />
                      </td>
                    </tr>
                    <tr class="col-lg-6">
                      <td>
                        <label for="region">WHID Region</label><br>
                        <select id="region" >
                          <option value="IAD">IAD</option>
                          <option value="DUB">DUB</option>
                          <option value="NRT">NRT</option>
                          <option value="BOM">BOM</option>
                        </select>
                      </td>
                    </tr>
                    <tr class="col-lg-6">
                      <td>
                        <div class="form-check">
                          <input class="form-check-input" type="checkbox" value="" id="flexCheckDefault" />
                          <label class="form-check-label" for="flexCheckDefault">Default checkbox</label>
                        </div>
                      </td>
                    </tr>
                    <tr class="col-lg-6">
                      <td>
                        <div class="form-check">
                          <input class="form-check-input" type="checkbox" value="" id="flexCheckDefault" />
                          <label class="form-check-label" for="flexCheckDefault">Default checkbox</label>
                        </div>
                      </td>
                    </tr>
                    <tr class="col-lg-6">
                      <td>
                        <div class="form-check">
                          <input class="form-check-input" type="checkbox" value="" id="flexCheckDefault" />
                          <label class="form-check-label" for="flexCheckDefault">Default checkbox</label>
                        </div>
                      </td>
                    </tr>
                  </tbody>
                </table>
              </div>
            </div>
          </div>
        </div>
      </div>
    </form>
  </div>
</template>

<script>
  /*  import gql from "graphql-tag";

  import findManyWHIDs from "~/graphql/query/findManyWHIDs"
  import findManyCategories from "~/graphql/query/findManyCategories"
  import findManyCountries from "~/graphql/query/findManyCountries"
  import attributes from "~/graphql/query/findManyAttributes"
  import findManyWHID_types from "~/graphql/query/findManyWHID_types"
  import findManyBrands from "~/graphql/query/findManyBrands"
  import findManydefaultTray from "~/graphql/query/findManydefaultTray"
  import findManyEvents from "~/graphql/query/findManyEvents"
  import manufacturerss from "~/graphql/query/manufacturers"
  import findManyTags from "~/graphql/query/findManyTags"
  import findManyduplexOption from "~/graphql/query/findManyduplexOption"

  const ADD_WHIDS = gql`
    mutation ($attributes: String!, $brand: String!, $categories: String!, $content: String!, $contract: String!, $cost_string: String!, $country: String!, $created_at: String!, $customer_type: String!, $family: String!, $file: String!, $region: String!, $status: String!, $id: String!, $image: String!, $manufacture: String!, $manufacturer_part_number: String!, $occassions: String!, $name: String!, $meta_url: String!, $meta_title: String!, $meta_keywords: String!, $meta_description: String!, $part_number: String!, $region: String!, $WHID: String!, $ipAddress: String!, $related_WHID: String!, $salable_quantity: String!, $short_description: String!, $defaultPaperSize: String!, $sku: String!, $status: String!, $WHIDFunction: String!, $tags: String!, $subnet: String!, $thumbnail: String!, $types: String!, $variants: String!, $visibility: String!, $websites: String!, $whid: String!, $zone: String!){
    createOneWHIDs(data: {attributes: $attributes, brand: $brand, categories: $categories, content: $content, contract: $contract, cost_string: $cost_string, country: $country, created_at: $created_at, customer_type: $customer_type, family: $family, file: $file, region: $region, status: $status, id: $id, image: $image, manufacture: $manufacture, manufacturer_part_number: $manufacturer_part_number, occassions: $occassions, name: $name, meta_url: $meta_url, meta_title: $meta_title, meta_keywords: $meta_keywords, meta_description: $meta_description, part_number: $part_number, region: $region, WHID: $WHID, ipAddress: $ipAddress, related_WHID: $related_WHID, salable_quantity: $salable_quantity, short_description: $short_description, defaultPaperSize: $defaultPaperSize, sku: $sku, status: $status, WHIDFunction: $WHIDFunction, tags: $tags, subnet: $subnet, thumbnail: $thumbnail, types: $types, variants: $variants, visibility: $visibility, websites: $websites, whid: $whid, zone: $zone}) {
        attributes
        brand
        categories
        content
        contract
        cost_string
        country
        created_at
        customer_type
        family
        file
        region
        status
        id
        image
        manufacture
        manufacturer_part_number
        occassions
        name
        meta_url
        meta_title
        meta_keywords
        meta_description
        part_number
        region
        WHID
        ipAddress
        related_WHID
        salable_quantity
        short_description
        defaultPaperSize
        sku
        status
        WHIDFunction
        tags
        subnet
        thumbnail
        types
        variants
        visibility
        websites
        whid
        zone
  }
}`;


  export default {
    data() {
      return {
        attributes: [],
        brand: [],
        categories: [],
        content: " ",
        contract: [],
        cost_string: " ",
        country: [],
        created_at: " ",
        customer_type: " ",
        family: " ",
        file: " ",
        region: " ",
        status: " ",
        id: " ",
        image: " ",
        manufacture: [],
        manufacturer_part_number: " ",
        occassions: [],
        name: " ",
        meta_url: " ",
        meta_title: " ",
        meta_keywords: " ",
        meta_description: " ",
        part_number: " ",
        region: " ",
        WHID: [],
        ipAddress: " ",
        related_WHID: " ",
        salable_quantity: " ",
        short_description: " ",
        defaultPaperSize: " ",
        sku: " ",
        status: " ",
        WHIDFunction: " ",
        tags: [],
        subnet: " ",
        thumbnail: " ",
        types: [],
        variants: " ",
        visibility: " ",
        websites: " ",
        whid: " ",
        zone: [],
        show: true
      }
    },
    head: {
      title: 'Add New WHID'
    },

    methods: {
      async addWHID() {
        const attributes = this.attributes;
        const brand = this.brand;
        const categories = this.categories;
        const content = this.content;
        const contract = this.contract;
        const cost_string = this.cost_string;
        const country = this.country;
        const created_at = this.created_at;
        const customer_type = this.customer_type;
        const family = this.family;
        const file = this.file;
        const region = this.region;
        const status = this.status;
        const id = this.id;
        const image = this.image;
        const manufacture = this.manufacture;
        const manufacturer_part_number = this.manufacturer_part_number;
        const occassions = this.occassions;
        const name = this.name;
        const meta_url = this.meta_url;
        const meta_title = this.meta_title;
        const meta_keywords = this.meta_keywords;
        const meta_description = this.meta_description;
        const part_number = this.part_number;
        const region = this.region;
        const WHID = this.WHID;
        const ipAddress = this.ipAddress;
        const related_WHID = this.related_WHID;
        const salable_quantity = this.salable_quantity;
        const short_description = this.short_description;
        const defaultPaperSize = this.defaultPaperSize;
        const sku = this.sku;
        const status = this.status;
        const WHIDFunction = this.WHIDFunction;
        const tags = this.tags;
        const subnet = this.subnet;
        const thumbnail = this.thumbnail;
        const types = this.types;
        const variants = this.variants;
        const visibility = this.visibility;
        const websites = this.websites;
        const whid = this.whid;
        const zone = this.zone;


        await this.$apollo.mutate({
          mutation: ADD_WHIDS,
          variables: {
            attributes,
            brand,
            categories,
            content,
            contract,
            cost_string,
            country,
            created_at,
            customer_type,
            family,
            file,
            region,
            status,
            id,
            image: target.files[0],
            manufacture,
            manufacturer_part_number,
            occassions,
            name,
            meta_url,
            meta_title,
            meta_keywords,
            meta_description,
            part_number,
            region,
            WHID,
            ipAddress,
            related_WHID,
            salable_quantity,
            short_description,
            defaultPaperSize,
            sku,
            status,
            WHIDFunction,
            tags,
            subnet,
            thumbnail,
            types,
            variants,
            visibility,
            websites,
            whid,
            zone,
          },
          update: (cache, {
            data: {
              insertCategories,
              insertCountries,
              insertAttributes,
              insertWHID_types,
              insertBrands,
              insertOccassions,
              insertduplexOption,
              insertTags,
              insertmanufacturer,
              insertWHIDs,
              insertdefaultTray
            }
          }) => {
            // Read data from cache for this query
            try {
              const insertedCategory = insertCategories.returning;
              const insertedCountries = insertCountries.returning;
              const insertedAttributes = insertAttributes.returning;
              const insertedWHID_types = insertWHID_types.returning;
              const insertedBrands = insertBrands.returning;
              const insertedOccassions = insertOccassions.returning;
              const insertedduplexOption = insertduplexOption.returning;
              const insertedTags = insertTags.returning;
              const insertedmanufacturer = insertmanufacturer.returning;
              const insertedWHIDs = insertWHIDs.returning;
              const inserteddefaultTray = insertdefaultTray.returning;
              console.log(insertedCategory, insertedCountries, insertedAttributes, insertedWHID_types,
                insertedBrands, insertedOccassions, insertedduplexOption, insertedTags, insertedmanufacturer,
                insertedWHIDs, inserteddefaultTray)
              cache.writeQuery({
                query: findManyWHIDs
              })
            } catch (err) {
              console.error(err)
            }
          }
        }).then(() => {
          this.$router.push({
            path: '../../shop/WHIDs'
          })
        }).catch(err => console.log(err));
        this.attributes = ' ';
        this.brand = ' ';
        this.categories = ' ';
        this.content = ' ';
        this.contract = ' ';
        this.cost_string = ' ';
        this.country = ' ';
        this.created_at = ' ';
        this.customer_type = ' ';
        this.family = ' ';
        this.file = ' ';
        this.region = ' ';
        this.status = ' ';
        this.id = ' ';
        this.image = ' ';
        this.manufacture = ' ';
        this.manufacturer_part_number = ' ';
        this.occassions = ' ';
        this.name = ' ';
        this.meta_url = ' ';
        this.meta_title = ' ';
        this.meta_keywords = ' ';
        this.meta_description = ' ';
        this.part_number = ' ';
        this.region = ' ';
        this.WHID = ' ';
        this.ipAddress = ' ';
        this.related_WHID = ' ';
        this.salable_quantity = ' ';
        this.short_description = ' ';
        this.defaultPaperSize = ' ';
        this.sku = ' ';
        this.status = ' ';
        this.WHIDFunction = ' ';
        this.tags = ' ';
        this.subnet = ' ';
        this.thumbnail = ' ';
        this.types = ' ';
        this.variants = ' ';
        this.visibility = ' ';
        this.websites = ' ';
        this.whid = ' ';
        this.zone = ' ';
      },
    },
    apollo: {
      findManyCategories: {
        prefetch: true,
        query: findManyCategories
      },
      findManyCountries: {
        prefetch: true,
        query: findManyCountries
      },
      attributes: {
        prefetch: true,
        query: attributes
      },
      findManyWHID_types: {
        prefetch: true,
        query: findManyWHID_types
      },
      findManyBrands: {
        prefetch: true,
        query: findManyBrands
      },
      findManydefaultTray: {
        prefetch: true,
        query: findManydefaultTray
      },
      manufacturerss: {
        prefetch: true,
        query: manufacturerss
      },
      findManyEvents: {
        prefetch: true,
        query: findManyEvents
      },
      findManyTags: {
        prefetch: true,
        query: findManyTags
      },
      findManyduplexOption: {
        prefetch: true,
        query: findManyduplexOption
      },
      findManyWHIDs: {
        prefetch: true,
        query: findManyWHIDs
      }
    }
  } */

</script>

<style>
  input,
  select,
  option {
    padding: 5px;
  }

</style>
