<template>
    <div>
        <div class="content-section introduction">
            <div class="feature-intro">
                <h1>TabView</h1>
                <p>TabView is a container component to group content with tabs.</p>
            </div>
        </div>

        <div class="content-section implementation">
            <h3 class="first">Default</h3>
            <p-tabView>
                <p-tabPanel header="Godfather I">
                    The story begins as Don Vito Corleone, the head of a New York Mafia family, overseeshis daughter's wedding. His beloved son ichael has just come home from the war, 
                    but does not intend to become part of his father's business. Through Michael's life the nature of the family business becomes clear. The business of the family is 
                    just like the head of the family, kind and benevolent to those who give respect, but given to ruthless violence whenever anything stands against the good of the family.
                </p-tabPanel>
                <p-tabPanel header="Godfather II">
                    Francis Ford Coppola's legendary continuation and sequel to his landmark 1972 film, TheGodfather parallels the young Vito Corleone's rise with his son Michael's spiritual fall, 
                    deepening The Godfather's depiction of the dark side of the American dream. In the early 1900s, the child Vito flees his Sicilian village for America after the local Mafia kills 
                    his family. Vito struggles to make a living, legally or illegally, for his wife and growing brood in Little Italy.
                </p-tabPanel>
                <p-tabPanel header="Godfather III">
                    The Godfather Part III is set in 1979 and 1980. Michael has moved back to New York and taken great strides to remove the family from crime. He turns over his New York criminal 
                    interests to longtime enforcer Joey Zasa. He uses his wealth in an attempt to rehabilitate his reputation through numerous philanthropic acts, administered by a foundation named after his father. 
                    A decade earlier, he gave custody of his two children to Kay, who has since remarried.
                </p-tabPanel>
            </p-tabView>

            <h3>Programmatic</h3>
            <div style="padding: .5em 0">
                <p-button icon="pi pi-chevron-left" @click="prev" class="p-button-secondary" />
                <p-button icon="pi pi-chevron-right" @click="next" style="margin-left: .5em" class="p-button-secondary"/>
            </div>

            <p-tabView>
                <p-tabPanel header="Godfather I" :active="activeIndex === 0">
                    The story begins as Don Vito Corleone, the head of a New York Mafia family, overseeshis daughter's wedding. His beloved son ichael has just come home from the war, 
                    but does not intend to become part of his father's business. Through Michael's life the nature of the family business becomes clear. The business of the family is 
                    just like the head of the family, kind and benevolent to those who give respect, but given to ruthless violence whenever anything stands against the good of the family.
                </p-tabPanel>
                <p-tabPanel header="Godfather II" :active="activeIndex === 1">
                    Francis Ford Coppola's legendary continuation and sequel to his landmark 1972 film, TheGodfather parallels the young Vito Corleone's rise with his son Michael's spiritual fall, 
                    deepening The Godfather's depiction of the dark side of the American dream. In the early 1900s, the child Vito flees his Sicilian village for America after the local Mafia kills 
                    his family. Vito struggles to make a living, legally or illegally, for his wife and growing brood in Little Italy.
                </p-tabPanel>
                <p-tabPanel header="Godfather III" :active="activeIndex === 2">
                    The Godfather Part III is set in 1979 and 1980. Michael has moved back to New York and taken great strides to remove the family from crime. He turns over his New York criminal 
                    interests to longtime enforcer Joey Zasa. He uses his wealth in an attempt to rehabilitate his reputation through numerous philanthropic acts, administered by a foundation named after his father. 
                    A decade earlier, he gave custody of his two children to Kay, who has since remarried.
                </p-tabPanel>
            </p-tabView>

            <h3>Disabled</h3>
            <p-tabView>
                <p-tabPanel header="Godfather I">
                    The story begins as Don Vito Corleone, the head of a New York Mafia family, overseeshis daughter's wedding. His beloved son ichael has just come home from the war, 
                    but does not intend to become part of his father's business. Through Michael's life the nature of the family business becomes clear. The business of the family is 
                    just like the head of the family, kind and benevolent to those who give respect, but given to ruthless violence whenever anything stands against the good of the family.
                </p-tabPanel>
                <p-tabPanel header="Godfather II">
                    Francis Ford Coppola's legendary continuation and sequel to his landmark 1972 film, TheGodfather parallels the young Vito Corleone's rise with his son Michael's spiritual fall, 
                    deepening The Godfather's depiction of the dark side of the American dream. In the early 1900s, the child Vito flees his Sicilian village for America after the local Mafia kills 
                    his family. Vito struggles to make a living, legally or illegally, for his wife and growing brood in Little Italy.
                </p-tabPanel>
                <p-tabPanel header="Godfather III">
                    The Godfather Part III is set in 1979 and 1980. Michael has moved back to New York and taken great strides to remove the family from crime. He turns over his New York criminal 
                    interests to longtime enforcer Joey Zasa. He uses his wealth in an attempt to rehabilitate his reputation through numerous philanthropic acts, administered by a foundation named after his father. 
                    A decade earlier, he gave custody of his two children to Kay, who has since remarried.
                </p-tabPanel>
                 <p-tabPanel header="Godfather IV" :disabled="true"></p-tabPanel>
            </p-tabView>

            <h3>Custom Headers</h3>
            <p-tabView class="tabview-custom">
                <p-tabPanel>
                    <template slot="header">
                        <i class="pi pi-calendar"></i>
                        <span>Godfather I</span>
                    </template> 
                    The story begins as Don Vito Corleone, the head of a New York Mafia family, overseeshis daughter's wedding. His beloved son ichael has just come home from the war, 
                    but does not intend to become part of his father's business. Through Michael's life the nature of the family business becomes clear. The business of the family is 
                    just like the head of the family, kind and benevolent to those who give respect, but given to ruthless violence whenever anything stands against the good of the family.
                </p-tabPanel>
                <p-tabPanel>
                    <template slot="header">
                        <span>Godfather II</span>
                        <i class="pi pi-user"></i>
                    </template> 
                    Francis Ford Coppola's legendary continuation and sequel to his landmark 1972 film, TheGodfather parallels the young Vito Corleone's rise with his son Michael's spiritual fall, 
                    deepening The Godfather's depiction of the dark side of the American dream. In the early 1900s, the child Vito flees his Sicilian village for America after the local Mafia kills 
                    his family. Vito struggles to make a living, legally or illegally, for his wife and growing brood in Little Italy.
                </p-tabPanel>
                <p-tabPanel>
                    <template slot="header">
                        <i class="pi pi-search"></i>
                        <span>Godfather III</span>
                        <i class="pi pi-cog"></i>
                    </template> 
                    The Godfather Part III is set in 1979 and 1980. Michael has moved back to New York and taken great strides to remove the family from crime. He turns over his New York criminal 
                    interests to longtime enforcer Joey Zasa. He uses his wealth in an attempt to rehabilitate his reputation through numerous philanthropic acts, administered by a foundation named after his father. 
                    A decade earlier, he gave custody of his two children to Kay, who has since remarried.
                </p-tabPanel>
            </p-tabView>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            activeIndex: 0
        }
    },
    methods: {
        next() {
            this.activeIndex = this.activeIndex === 2 ? 0 : this.activeIndex + 1;
        },
        prev() {
            this.activeIndex = this.activeIndex === 0 ? 2 : this.activeIndex - 1;
        }
    }
}
</script>

<style lang="scss" scoped>
.tabview-custom {
    i, span {
        vertical-align: middle;
    }

    span {
        margin: 0 .5em;
    }
}
</style>