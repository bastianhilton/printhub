<template>
  <div>
    <form  @submit.prevent="addPrinter">
      <nav class="navbar navbar-dark bg-dark">
        <div class="container-fluid">
          <a class="navbar-brand">
            <button type="reset" class="btn btn-warning">Reset</button></a>
          <a class="navbar-brand">
            <input type="submit" class="btn btn-warning" value="Save Printer" /></a>
        </div>
      </nav>
      <br>
      <div class="row">
        <div class="col-3">
          <!-- Tab navs -->
          <div id="v-tabs-tab" class="nav flex-column nav-tabs text-center" role="tablist" aria-orientation="vertical">
            <a id="v-tabs-home-tab" class="nav-link active" data-mdb-toggle="tab" href="#v-tabs-home" role="tab"
              aria-controls="v-tabs-home" aria-selected="true">Create A New Printer</a>
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
                        <label for="type">Printer Types</label><br>
                        <select id="PrinterType" v-model="types" name="template" class="form-attribute">
                          <option v-for="types in findManyPrinter_types" :key="types.id" :value="Printer_types">{{ types.name }}
                          </option>
                        </select>
                      </td>
                    </tr>
                    <tr class="col-lg-6">
                      <td>
                        <input v-model="name" type="text" required value="Printer Name" />
                      </td>
                    </tr>
                    <tr class="col-lg-6">
                      <td>
                        <input v-model="mac" type="number" placeholder="$" value="Printer mac" required />
                      </td>
                    </tr>
                    <tr class="col-lg-6">
                      <td>
                        <input v-model="subnet" name="PrinterTax" value="Tax Class" type="text" />
                      </td>
                    </tr>
                    <tr class="col-lg-6">
                      <td>
                        <input v-model="ipAddress" type="number" value="Quantity" />
                      </td>
                    </tr>
                    <tr class="col-lg-6">
                      <td>
                        <select id="stockStatus" v-model="printerFunction">
                          <option value="inStock">In Stock</option>
                          <option value="outStock">Out of Stock</option>
                          <option value="backorder">Backorder</option>
                          <option value="clearance">Clearance</option>
                        </select>
                      </td>
                    </tr>
                    <tr class="col-lg-6">
                      <td>
                        <select id="stockStatus" v-model="defaultTray">
                          <option value="inStock">In Stock</option>
                          <option value="outStock">Out of Stock</option>
                          <option value="backorder">Backorder</option>
                          <option value="clearance">Clearance</option>
                        </select>
                      </td>
                    </tr>
                    <tr class="col-lg-6">
                      <td>
                        <input v-model="status" type="number" value="Printer status" />
                      </td>
                    </tr>
                    <tr class="col-lg-6">
                      <td>
                        <input v-model="whid" type="number" value="Printer whid" />
                      </td>
                    </tr>
                    <tr class="col-lg-6">
                      <td>
                        <input v-model="driver" type="number" value="Printer Driver" />
                      </td>
                    </tr>
                    <tr class="col-lg-6">
                      <td>
                        <input v-model="duplexOption" type="number" value="Printer Duplex Option" />
                      </td>
                    </tr>
                    <tr class="col-lg-6">
                      <td>
                        <label for="tags">Tags</label><br>
                        <select id="category" v-model="tags">
                          <option v-for="tags in tags" :key="tags.id" :value="tags">
                            {{ tags.name }}</option>
                        </select>
                      </td>
                    </tr>
                    <tr class="col-lg-6">
                      <td>
                        <label for="zone">duplexOption</label><br>
                        <select id="zone" v-model="zone">
                          <option v-for="zone in findManyduplexOption" :key="zone.id" :value="zone">
                            {{ zone.name }}</option>
                        </select>
                      </td>
                    </tr>
                    <tr class="col-lg-6">
                      <td>
                        <select id="defaultPaperSize" v-model="defaultPaperSize">
                          <option value="petite">Petite</option>
                          <option value="xs">Extra Small</option>
                          <option value="small">Small</option>
                          <option value="medium">Medium</option>
                          <option value="large">Large</option>
                          <option value="xl">Extra Large</option>
                          <option value="xxl">XXL</option>
                          <option value="bigntall">Big and Tall</option>
                        </select>
                      </td>
                    </tr>
                    <tr class="col-lg-6">
                      <td>
                        <select id="colorOption" v-model="colorOption">
                          <option value="digital">Digital</option>
                          <option value="physical">Physical</option>
                          <option value="service">Service</option>
                          <option value="subscription">Subscription</option>
                        </select>
                      </td>
                    </tr>
                    <tr class="col-lg-12">
                      <td>
                        <label for="Printer">Related Printers</label><br>
                        <select id="Printer" v-model="Printer">
                          <option v-for="Printer in findManyPrinters" :key="Printer.id" :value="Printer">
                            {{ Printer.name }}</option>
                        </select>
                      </td>
                    </tr>
                  </tbody>
                </table>
              </div>
              <br><br>
              <div id="accordionExample" class="accordion">
                <div class="accordion-item">
                  <h2 id="headingOne" class="accordion-header">
                    <button class="accordion-button" type="button" data-mdb-toggle="collapse"
                      data-mdb-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
                      Printer Description
                    </button>
                  </h2>
                  <div id="collapseOne" class="accordion-collapse collapse" aria-labelledby="headingOne"
                    data-mdb-parent="#accordionExample">
                    <div class="accordion-body">
                      <div class="table table-responsive">
                        <table class="table">
                          <tbody>
                            <tr>
                              <td style="text-align: right;">Description</td>
                              <td>
                                <div class="form-check form-switch">
                                  <textarea v-model="description" cols="50" rows="10" value="Add a longer Description"></textarea>
                                </div>
                              </td>
                            </tr>
                          </tbody>
                        </table>
                      </div>
                    </div>
                  </div>
                </div>
                <div class="accordion-item">
                  <h2 id="headingThree" class="accordion-header">
                    <button class="accordion-button" type="button" data-mdb-toggle="collapse"
                      data-mdb-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
                      Printer Images
                    </button>
                  </h2>
                  <div id="collapseThree" class="accordion-collapse collapse" aria-labelledby="headingThree"
                    data-mdb-parent="#accordionExample">
                    <div class="accordion-body">
                      <td>
                        <div class="file-upload-wrapper">
                          <input type="file" id="input-file-now" class="file-upload-input"
                            data-mdb-file-upload="file-upload" data-mdb-accepted-extensions="image/*" />
                        </div>
                      </td>
                    </div>
                  </div>
                </div>
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

  import findManyPrinters from "~/graphql/query/findManyPrinters"
  import findManyCategories from "~/graphql/query/findManyCategories"
  import findManyCountries from "~/graphql/query/findManyCountries"
  import attributes from "~/graphql/query/findManyAttributes"
  import findManyPrinter_types from "~/graphql/query/findManyPrinter_types"
  import findManyBrands from "~/graphql/query/findManyBrands"
  import findManydefaultTray from "~/graphql/query/findManydefaultTray"
  import findManyEvents from "~/graphql/query/findManyEvents"
  import manufacturerss from "~/graphql/query/manufacturers"
  import findManyTags from "~/graphql/query/findManyTags"
  import findManyduplexOption from "~/graphql/query/findManyduplexOption"

  const ADD_PrinterS = gql`
    mutation ($attributes: String!, $brand: String!, $categories: String!, $content: String!, $contract: String!, $cost_string: String!, $country: String!, $created_at: String!, $customer_type: String!, $family: String!, $file: String!, $colorOption: String!, $status: String!, $id: String!, $image: String!, $manufacture: String!, $manufacturer_part_number: String!, $occassions: String!, $name: String!, $meta_url: String!, $meta_title: String!, $meta_keywords: String!, $meta_description: String!, $part_number: String!, $mac: String!, $Printer: String!, $ipAddress: String!, $related_Printer: String!, $salable_quantity: String!, $short_description: String!, $defaultPaperSize: String!, $sku: String!, $status: String!, $printerFunction: String!, $tags: String!, $subnet: String!, $thumbnail: String!, $types: String!, $variants: String!, $visibility: String!, $websites: String!, $whid: String!, $zone: String!){
    createOnePrinters(data: {attributes: $attributes, brand: $brand, categories: $categories, content: $content, contract: $contract, cost_string: $cost_string, country: $country, created_at: $created_at, customer_type: $customer_type, family: $family, file: $file, colorOption: $colorOption, status: $status, id: $id, image: $image, manufacture: $manufacture, manufacturer_part_number: $manufacturer_part_number, occassions: $occassions, name: $name, meta_url: $meta_url, meta_title: $meta_title, meta_keywords: $meta_keywords, meta_description: $meta_description, part_number: $part_number, mac: $mac, Printer: $Printer, ipAddress: $ipAddress, related_Printer: $related_Printer, salable_quantity: $salable_quantity, short_description: $short_description, defaultPaperSize: $defaultPaperSize, sku: $sku, status: $status, printerFunction: $printerFunction, tags: $tags, subnet: $subnet, thumbnail: $thumbnail, types: $types, variants: $variants, visibility: $visibility, websites: $websites, whid: $whid, zone: $zone}) {
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
        colorOption
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
        mac
        Printer
        ipAddress
        related_Printer
        salable_quantity
        short_description
        defaultPaperSize
        sku
        status
        printerFunction
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
        colorOption: " ",
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
        mac: " ",
        Printer: [],
        ipAddress: " ",
        related_Printer: " ",
        salable_quantity: " ",
        short_description: " ",
        defaultPaperSize: " ",
        sku: " ",
        status: " ",
        printerFunction: " ",
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
      title: 'Add New Printer'
    },

    methods: {
      async addPrinter() {
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
        const colorOption = this.colorOption;
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
        const mac = this.mac;
        const Printer = this.Printer;
        const ipAddress = this.ipAddress;
        const related_Printer = this.related_Printer;
        const salable_quantity = this.salable_quantity;
        const short_description = this.short_description;
        const defaultPaperSize = this.defaultPaperSize;
        const sku = this.sku;
        const status = this.status;
        const printerFunction = this.printerFunction;
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
          mutation: ADD_PrinterS,
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
            colorOption,
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
            mac,
            Printer,
            ipAddress,
            related_Printer,
            salable_quantity,
            short_description,
            defaultPaperSize,
            sku,
            status,
            printerFunction,
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
              insertPrinter_types,
              insertBrands,
              insertOccassions,
              insertduplexOption,
              insertTags,
              insertmanufacturer,
              insertPrinters,
              insertdefaultTray
            }
          }) => {
            // Read data from cache for this query
            try {
              const insertedCategory = insertCategories.returning;
              const insertedCountries = insertCountries.returning;
              const insertedAttributes = insertAttributes.returning;
              const insertedPrinter_types = insertPrinter_types.returning;
              const insertedBrands = insertBrands.returning;
              const insertedOccassions = insertOccassions.returning;
              const insertedduplexOption = insertduplexOption.returning;
              const insertedTags = insertTags.returning;
              const insertedmanufacturer = insertmanufacturer.returning;
              const insertedPrinters = insertPrinters.returning;
              const inserteddefaultTray = insertdefaultTray.returning;
              console.log(insertedCategory, insertedCountries, insertedAttributes, insertedPrinter_types,
                insertedBrands, insertedOccassions, insertedduplexOption, insertedTags, insertedmanufacturer,
                insertedPrinters, inserteddefaultTray)
              cache.writeQuery({
                query: findManyPrinters
              })
            } catch (err) {
              console.error(err)
            }
          }
        }).then(() => {
          this.$router.push({
            path: '../../shop/Printers'
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
        this.colorOption = ' ';
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
        this.mac = ' ';
        this.Printer = ' ';
        this.ipAddress = ' ';
        this.related_Printer = ' ';
        this.salable_quantity = ' ';
        this.short_description = ' ';
        this.defaultPaperSize = ' ';
        this.sku = ' ';
        this.status = ' ';
        this.printerFunction = ' ';
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
      findManyPrinter_types: {
        prefetch: true,
        query: findManyPrinter_types
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
      findManyPrinters: {
        prefetch: true,
        query: findManyPrinters
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
