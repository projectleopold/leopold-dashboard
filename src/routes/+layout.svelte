<!--
  - Copyright 2023 The Project Leopold Authors
  -
  - Licensed under the Apache License, Version 2.0 (the "License");
  - you may not use this file except in compliance with the License.
  - You may obtain a copy of the License at
  -
  -     http://www.apache.org/licenses/LICENSE-2.0
  -
  - Unless required by applicable law or agreed to in writing, software
  - distributed under the License is distributed on an "AS IS" BASIS,
  - WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
  - See the License for the specific language governing permissions and
  - limitations under the License.
  -->

<script lang='ts'>
    import '@skeletonlabs/skeleton/themes/theme-rocket.css';
    import '@skeletonlabs/skeleton/styles/skeleton.css';
    import '../app.postcss';
    import { AppBar, AppShell, autoModeWatcher, LightSwitch } from '@skeletonlabs/skeleton';
</script>

<svelte:head>
    {@html `<script>${autoModeWatcher.toString()} autoModeWatcher();</script>`}
</svelte:head>

<AppShell>
    <svelte:fragment slot="header">
        <AppBar padding="p-2">
            <svelte:fragment slot="lead">
                <strong class="text-xl uppercase">Leopold</strong>
            </svelte:fragment>
            <svelte:fragment slot="trail">
                <a
                        class="btn btn-sm variant-ghost-surface"
                        href="https://github.com/projectleopold"
                        target="_blank"
                        rel="noreferrer"
                >
                    GitHub
                </a>
                <LightSwitch />
            </svelte:fragment>
        </AppBar>
    </svelte:fragment>
    <slot />
    <svelte:fragment slot="pageFooter">
        <AppBar padding="p-1">
            <svelte:fragment slot="lead">
                <strong>
                    &copy; 2023
                    <a
                            class="anchor"
                            href="https://projectleopold.github.io"
                            target="_blank"
                            rel="noreferrer"
                    >
                        Project Leopold
                    </a>
                </strong>
            </svelte:fragment>
        </AppBar>
    </svelte:fragment>
</AppShell>
