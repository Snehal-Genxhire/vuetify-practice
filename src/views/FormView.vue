<template>
    <AutoCompletes/>
    <CheckboxComponenet/>
    <ComboBox/>
    <FileInputs/>
    <Form />
    <RangeSlider />
    <Select/>
    <Sliders/>
    <Switches/>
<TextFields/>
</template>

<script>
import AutoCompletes from '@/components/FormControls/AutoCompletes.vue'
import CheckboxComponenet from '@/components/FormControls/CheckboxComponenet.vue'
import ComboBox from '@/components/FormControls/ComboBox.vue'
import FileInputs from '@/components/FormControls/FileInputs.vue'
import Form from '@/components/FormControls/Form.vue'
import RangeSlider from '@/components/FormControls/RangeSlider.vue'
import Select from '@/components/FormControls/Select.vue'
import Sliders from '@/components/FormControls/Sliders.vue'
import Switches from '@/components/FormControls/Switches.vue'
import TextFields from '@/components/FormControls/TextFields.vue'


export default {
    name: "FormView",
    components: { AutoCompletes, CheckboxComponenet, FileInputs, ComboBox, Form, RangeSlider, Select, Sliders, Switches, TextFields }
}
</script>